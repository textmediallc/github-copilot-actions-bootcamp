## Lab 17: Manual Workflow Dispatch with Inputs

**Real-World Scenario:** Sometimes QA needs to trigger a deployment to the staging environment manually, and they want to specify exactly which branch or feature flag to deploy.

**Why We Are Doing This:** The `workflow_dispatch` trigger turns GitHub Actions into a self-service portal. It allows non-developers (like QA or Product Managers) to run complex automations by simply filling out a form in the GitHub UI.

### Step-by-Step Instructions
1. Create a new workflow file named `manual-deploy.yml`.
2. Open Copilot Chat and type: *"Write a GitHub Actions workflow that uses the `workflow_dispatch` trigger. It should have two inputs: a boolean called 'run_migrations' (default false) and a choice called 'environment' (options: staging, production)."*
3. Add a simple step to echo these inputs:
   ```yaml
   - run: echo "Deploying to ${{ github.event.inputs.environment }}. Run migrations: ${{ github.event.inputs.run_migrations }}"
   ```
4. Commit and push.
5. Go to the Actions tab on GitHub, click your new workflow on the left, and click the **Run workflow** button. Fill out the form and watch the result!

---
