## Lab 10: Your First Reusable Workflow

**Real-World Scenario:** Your organization has 50 Node.js repositories. Instead of copy-pasting the same lint and test YAML into 50 repos, your platform team wants to maintain one central "canonical" CI workflow that all other repos call.

**Why We Are Doing This:** Reusable workflows enforce standardization across an enterprise and drastically reduce maintenance overhead. If you need to update the Node version, you change it in one place, and all 50 repos instantly inherit the change.

### Step-by-Step Instructions
1. Create a new repository called `shared-actions-org` (or similar).
2. Inside it, create the directory structure: `.github/workflows/`.
3. Create a file named `node-ci-reusable.yml`.
4. Open Copilot Chat and type: *"Write a reusable GitHub Actions workflow (using `workflow_call`) that checks out code, sets up Node.js based on an input parameter, runs `npm ci`, and runs `npm test`."*
5. Review the generated YAML. Ensure it includes:
   ```yaml
   on:
     workflow_call:
       inputs:
         node-version:
           required: true
           type: string
   ```
6. Commit and push this file to the `main` branch.

---
