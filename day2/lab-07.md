## Lab 7: Project Management with GitHub Issues & Projects
**Scenario:** You need to organize the upcoming sprint. You will create issues, link them to a project board, and use keywords to auto-close them.
**Why We Are Doing This:** Keeping code and project management in the same tool reduces context switching and provides full traceability from bug report to code fix.

**Step-by-Step Instructions:**
1. In your repository, click the **Issues** tab and create a new issue titled "Fix login validation bug".
2. Click the **Projects** tab at the top of the repository and create a new **Board** (Kanban style).
3. Add your new issue to the "Todo" column of the project board.
4. In VS Code, create a branch, make a code change, and commit it.
5. Push the branch and open a PR. In the PR description, type exactly: `Closes #1` (assuming your issue is ID #1).
6. Merge the PR. Notice that GitHub automatically closed the issue and moved it to the "Done" column on your project board!

---
