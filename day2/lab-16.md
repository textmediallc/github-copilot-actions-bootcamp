## Lab 16: Passing Artifacts Between Jobs

**Real-World Scenario:** Your CI pipeline has two distinct jobs: `build` and `deploy`. The `build` job compiles your React app into a `dist/` folder. The `deploy` job needs to upload that folder to a server.

**Why We Are Doing This:** Jobs in GitHub Actions run on completely fresh, isolated virtual machines. Files created in Job A do not exist in Job B unless you explicitly upload and download them as Artifacts.

### Step-by-Step Instructions
1. Create a workflow with two jobs: `build` and `deploy`.
2. Ensure `deploy` has `needs: build`.
3. In the `build` job, use Copilot to generate a step that uploads the `dist/` folder.
   *Prompt:* *"Add a step to upload the 'dist' directory as an artifact named 'build-output' using actions/upload-artifact@v4"*
4. In the `deploy` job, use Copilot to generate a step that downloads it.
   *Prompt:* *"Add a step to download the 'build-output' artifact using actions/download-artifact@v4"*
5. Commit and push. Verify in the Actions UI that the artifact was successfully passed between the two isolated runners.

---
