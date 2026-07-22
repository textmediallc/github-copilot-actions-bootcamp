## Lab 3: Branching Strategies and Feature Isolation
**Real-World Scenario:** You need to add a new database connection feature to the inventory service, but the main branch must remain stable and deployable at all times.
**Why we are doing this:** Branching allows multiple developers to work on different features simultaneously without breaking the production code.

### Step-by-Step Instructions:
1. **Check Current Branch:**
   * Run: `git branch` (Ensure you are on `main` or `master`).
2. **Create and Switch to a Feature Branch:**
   * Run: `git checkout -b feature/db-connection`
   * *Explanation:* The `-b` flag creates the branch and switches to it in one step. Your work is now isolated.
3. **Make Changes on the Branch:**
   * Open `index.js` and add: `const db = require('./db'); console.log('Connecting to DB...');`
   * Save the file.
4. **Stage and Commit the Feature:**
   * Run: `git add index.js`
   * Run: `git commit -m "feat: Add database connection initialization"`
5. **Switch Back to Main:**
   * Run: `git checkout main`
   * Look at `index.js` in your editor.
   * *Explanation:* Notice that the database code is gone! The `main` branch is untouched by your experimental feature.

---
