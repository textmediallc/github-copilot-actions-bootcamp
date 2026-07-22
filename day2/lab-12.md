## Lab 12: Creating a Composite Action

**Real-World Scenario:** You have a sequence of three steps that you run in almost every job: checking out the code, setting up Node, and configuring caching. You want to bundle these three steps into a single custom Action.

**Why We Are Doing This:** While reusable workflows share entire *jobs* or *workflows*, Composite Actions let you package a sequence of *steps* into a single `uses:` command. It's the ultimate tool for keeping YAML DRY (Don't Repeat Yourself).

### Step-by-Step Instructions
1. In your repository, create a folder structure: `.github/actions/setup-node-env/`.
2. Inside that folder, create a file named `action.yml` (it *must* be named `action.yml`).
3. Open Copilot Chat and type: *"Write a composite GitHub Action `action.yml` that checks out the repository, sets up Node.js v20, and configures npm caching."*
4. Ensure the output contains `runs: using: "composite"` and that every step has `shell: bash` (a requirement for composite actions).
   ```yaml
   runs:
     using: "composite"
     steps:
       - uses: actions/checkout@v4
       - uses: actions/setup-node@v4
         with:
           node-version: '20'
           cache: 'npm'
       - run: npm ci
         shell: bash
   ```
5. Commit and push. You can now use `uses: ./.github/actions/setup-node-env` in your main workflow!

---
