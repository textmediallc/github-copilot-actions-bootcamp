## Lab 2: Setting up CODEOWNERS
**Scenario:** You want to ensure that any changes to database configuration files are automatically reviewed by the backend team lead.
**Why We Are Doing This:** CODEOWNERS automates the PR review process, ensuring that the right domain experts are notified when specific files are modified.

**Step-by-Step Instructions:**
1. In your repository, create a new branch: `git checkout -b feature/codeowners`
2. Create a hidden directory called `.github` in the root of your project: `mkdir .github`
3. Create a file named `CODEOWNERS` inside that directory.
4. Add the following line to the file, replacing `@your-github-username` with your actual username:
   ```text
   *.js @your-github-username
   ```
5. Commit and push the branch:
   ```bash
   git add .github/CODEOWNERS
   git commit -m "Add CODEOWNERS file"
   git push origin feature/codeowners
   ```
6. Open a Pull Request on GitHub. Once merged, any future PR that modifies a `.js` file will automatically request a review from you!

---
