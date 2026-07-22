## Lab 11: Calling a Reusable Workflow

**Real-World Scenario:** You are a product developer. The platform team just published the reusable workflow from Lab 1. You need to hook your new API project up to it.

**Why We Are Doing This:** This teaches the "consumer" side of reusable workflows. It shows how incredibly simple a repository's CI file becomes when the heavy lifting is abstracted away.

### Step-by-Step Instructions
1. Open your main mini-app repository from earlier today.
2. Delete your existing `.github/workflows/ci.yml` file (or rename it to `ci.yml.old`).
3. Create a new `.github/workflows/ci.yml`.
4. Open Copilot Chat and type: *"Write a GitHub Actions workflow that triggers on push to main. It should have one job that calls a reusable workflow located at `[YOUR_USERNAME]/shared-actions-org/.github/workflows/node-ci-reusable.yml@main`. Pass '20' as the `node-version` input."*
5. The generated YAML should look something like this:
   ```yaml
   jobs:
     call-shared-ci:
       uses: your-username/shared-actions-org/.github/workflows/node-ci-reusable.yml@main
       with:
         node-version: "20"
   ```
6. Commit and push. Go to the Actions tab on GitHub to watch it execute the steps defined in the other repository!

---
