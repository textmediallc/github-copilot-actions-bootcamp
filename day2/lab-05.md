## Lab 5: Matrix Builds for Cross-Platform Testing
**Scenario:** Your application needs to run on multiple versions of Node.js (18, 20, and 22) to ensure backward compatibility.
**Why We Are Doing This:** Matrix builds allow you to run the exact same job multiple times with different variables, saving you from writing duplicate YAML code.

**Step-by-Step Instructions:**
1. Open the `.github/workflows/ci.yml` file from Lab 4.
2. Modify the `build-and-test` job to include a strategy matrix:
   ```yaml
   jobs:
     build-and-test:
       runs-on: ubuntu-latest
       strategy:
         matrix:
           node-version: [18.x, 20.x, 22.x]
       steps:
       - uses: actions/checkout@v4
       - name: Use Node.js ${{ matrix.node-version }}
         uses: actions/setup-node@v4
         with:
           node-version: ${{ matrix.node-version }}
   ```
3. Commit and push. When you check the Actions tab, you will see *three* separate jobs running simultaneously, one for each Node version!

---
