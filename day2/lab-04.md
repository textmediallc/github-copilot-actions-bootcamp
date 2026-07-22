## Lab 4: Automating a Node.js CI Pipeline
**Scenario:** You have a Node.js application. You need to ensure that every PR passes the linter and unit tests before it can be merged.
**Why We Are Doing This:** This is a real-world Continuous Integration (CI) pipeline. It catches bugs automatically before they reach production.

**Step-by-Step Instructions:**
1. Ensure you have a basic `package.json` with a `test` script (even a dummy one).
2. Create a new file: `.github/workflows/ci.yml`
3. Add the following workflow definition:
   ```yaml
   name: Node.js CI
   on:
     pull_request:
       branches: [ main ]
   jobs:
     build-and-test:
       runs-on: ubuntu-latest
       steps:
       - name: Checkout code
         uses: actions/checkout@v4
       - name: Setup Node.js
         uses: actions/setup-node@v4
         with:
           node-version: '20'
           cache: 'npm'
       - name: Install dependencies
         run: npm ci
       - name: Run tests
         run: npm test
   ```
4. Notice the `cache: 'npm'` line. This speeds up future runs by saving the `node_modules` directory!
5. Commit, push, and open a PR to trigger the workflow.

---
