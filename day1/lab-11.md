## Lab 11: Git Survival Skill - Stashing Changes
**Real-World Scenario:** You are halfway through writing a new authentication feature when a critical bug is reported in production. You need to switch branches immediately to fix the bug, but your current code is broken and not ready to commit.
**Why we are doing this:** `git stash` allows you to temporarily shelve (stash) your incomplete changes so you can switch contexts without losing work or creating messy "WIP" (Work In Progress) commits.

### Step-by-Step Instructions:
1. **Create Unfinished Work:**
   * In your `ecommerce-inventory` repo, make sure you are on `main`.
   * Open `index.js` and add a half-finished function: `function loginUser() { // TODO: add auth logic`
   * Do not commit this.
2. **Attempt to Switch Branches (and fail):**
   * Run: `git checkout -b hotfix/crash`
   * *Explanation:* Git might let you switch if there are no conflicts, but the dirty working state comes with you, which is dangerous. Let's stash it instead.
3. **Stash the Changes:**
   * Run: `git stash save "WIP: auth logic"`
   * Look at `index.js`. Your half-finished code is gone. Your working directory is clean.
4. **Fix the Bug and Return:**
   * Switch to the hotfix branch: `git checkout -b hotfix/crash`
   * (Pretend you fix the bug and commit it).
   * Switch back to main: `git checkout main`
5. **Restore the Stash:**
   * Run: `git stash list` (to see your saved stash).
   * Run: `git stash pop`
   * *Explanation:* Your half-finished auth code is restored, and the stash is removed from the list. You can now resume your work exactly where you left off.

---
