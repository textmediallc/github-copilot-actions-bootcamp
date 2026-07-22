## Lab 12: Git Survival Skill - Resolving a Merge Conflict
**Real-World Scenario:** You and a coworker both edited the exact same line in the `README.md` file on different branches. When you try to merge your branch, Git doesn't know whose changes to keep.
**Why we are doing this:** Merge conflicts are inevitable in team environments. Learning to resolve them calmly in VS Code prevents panic and accidental code deletion.

### Step-by-Step Instructions:
1. **Set up the Conflict:**
   * On `main`, edit `README.md` to say: `Version 1.0 - Maintained by Alice`.
   * Commit the change: `git commit -am "Update README owner to Alice"`
2. **Create the Divergence:**
   * Run: `git checkout -b feature/readme-update`
   * Edit `README.md` to say: `Version 1.0 - Maintained by Bob`.
   * Commit the change: `git commit -am "Update README owner to Bob"`
3. **Force the Conflict:**
   * Switch back to main: `git checkout main`
   * Edit `README.md` again to say: `Version 1.0 - Maintained by Charlie`.
   * Commit the change: `git commit -am "Update README owner to Charlie"`
4. **Attempt the Merge:**
   * Run: `git merge feature/readme-update`
   * *Explanation:* Git will halt and announce a conflict in `README.md`.
5. **Resolve in VS Code:**
   * Open `README.md` in VS Code. You will see `<<<<<<< HEAD` and `======` markers.
   * Use the VS Code Code Lens buttons above the conflict to click **"Accept Both Changes"** or manually edit the text to say: `Version 1.0 - Maintained by Charlie and Bob`.
   * Save the file.
6. **Finalize the Merge:**
   * Run: `git add README.md`
   * Run: `git commit -m "Merge conflict resolved in README"`

---
