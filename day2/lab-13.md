## Lab 13: Copilot for Bash Scripting in Actions

**Real-World Scenario:** You need a custom step in your CI pipeline that checks if the `package.json` version number was incremented before allowing a merge to the `main` branch.

**Why We Are Doing This:** Writing inline bash scripts inside YAML can be tedious, especially when dealing with string parsing or JSON extraction. Copilot excels at writing these small, highly specific shell scripts.

### Step-by-Step Instructions
1. Open your CI workflow file.
2. Add a new step to your build job.
3. Above the step, write a comment: `# Use jq to extract the version from package.json and fail the step if it is '1.0.0'`
4. Press Enter and let Copilot generate the `run:` command.
5. It should generate something like:
   ```yaml
   - name: Check version
     run: |
       VERSION=$(jq -r '.version' package.json)
       if [ "$VERSION" = "1.0.0" ]; then
         echo "Error: Version must be incremented!"
         exit 1
       fi
   ```
6. Test it by running the action. Then change the version in `package.json` to `1.0.1` and watch it pass.

---
