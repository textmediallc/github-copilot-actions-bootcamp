## Lab 13: Git History - Reading the Log and Blame
**Real-World Scenario:** You discover a bug in the database connection string. You need to find out when this line was introduced and who wrote it so you can ask them for context.
**Why we are doing this:** `git log` and `git blame` are investigative tools. They turn your version control system into an audit trail, allowing you to track down the origin of any line of code.

### Step-by-Step Instructions:
1. **View the Log:**
   * Run: `git log --oneline --graph --all`
   * *Explanation:* This provides a condensed, visual representation of your repository's history and branching structure.
2. **Investigate a File (Blame):**
   * Open `index.js` in VS Code.
   * Right-click anywhere in the file and select **"Git: Open Changes"** (if using GitLens) or use the terminal.
   * In the terminal, run: `git blame index.js`
3. **Analyze the Output:**
   * Look at the output. Every line of `index.js` is prefixed with a commit hash, an author name, a timestamp, and the code itself.
   * *Explanation:* You can now see exactly who wrote the buggy line and the commit message associated with it, giving you the context needed to fix it safely.

---
