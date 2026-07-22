## Lab 1: Configuring Branch Protection Rules
**Scenario:** Your team is growing, and developers are accidentally pushing broken code directly to the `main` branch. You need to lock it down.
**Why We Are Doing This:** Branch protection is the foundation of enterprise GitHub usage. It forces all changes to go through Pull Requests and pass automated checks.

**Step-by-Step Instructions:**
1. Open your repository on GitHub.com.
2. Click the **Settings** tab at the top.
3. In the left sidebar, click **Branches** under the "Code and automation" section.
4. Click the **Add branch protection rule** button.
5. In the "Branch name pattern" box, type `main`.
6. Check the box for **Require a pull request before merging**.
7. Check the sub-box for **Require approvals** and set the number of required approvals to `1`.
8. Scroll to the bottom and click **Create**.
9. **Test it:** Open your terminal, make a small change to a file, commit it, and try to run `git push origin main`. You should receive an error from GitHub rejecting the push!

---
