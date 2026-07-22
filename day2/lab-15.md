## Lab 15: Using Copilot to Fix a Failing Action

**Real-World Scenario:** Your deployment workflow failed with a cryptic error message about missing permissions. You need to debug and fix it quickly.

**Why We Are Doing This:** Copilot isn't just for writing code; it's an incredible debugging assistant for DevOps. Pasting error logs into Copilot Chat is often much faster than searching Stack Overflow.

### Step-by-Step Instructions
1. Intentionally break your workflow by adding this step:
   ```yaml
   - run: npm publish
   ```
2. Commit and push. The Action will fail because you haven't provided an NPM token.
3. Go to the Actions tab, click on the failed job, and copy the raw error output from the logs.
4. Open Copilot Chat in VS Code and type: *"My GitHub Action failed with this error: [PASTE ERROR LOG]. How do I fix this?"*
5. Copilot will explain that you are missing the `NODE_AUTH_TOKEN` environment variable and provide the exact YAML snippet to fix it using `${{ secrets.NPM_TOKEN }}`.

---
