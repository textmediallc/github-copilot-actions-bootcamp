## Lab 9: Advanced Copilot: Generating CI/CD YAML
**Scenario:** Writing YAML syntax from memory is frustrating. You will use Copilot Chat to generate a complex deployment workflow.
**Why We Are Doing This:** Copilot is not just for application code; it is excellent at generating infrastructure-as-code and CI/CD pipelines.

**Step-by-Step Instructions:**
1. Open VS Code and open the Copilot Chat panel.
2. Enter the following prompt:
   *"Write a GitHub Actions workflow that triggers when a GitHub Release is published. It should checkout the code, setup Node 20, run `npm ci`, run `npm run build`, and then upload the `./dist` folder as a workflow artifact."*
3. Review the generated YAML. It should look very similar to this:
   ```yaml
   on:
     release:
       types: [published]
   jobs:
     build-and-upload:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v4
         - uses: actions/setup-node@v4
           with: { node-version: '20' }
         - run: npm ci
         - run: npm run build
         - uses: actions/upload-artifact@v4
           with:
             name: build-output
             path: ./dist
   ```
4. Click the **Insert at Cursor** button to add it to a new file in your `.github/workflows/` directory.
