## Lab 8: Using Dependabot for Security Updates
**Scenario:** Your project uses older npm packages that have known security vulnerabilities. You want GitHub to automatically update them for you.
**Why We Are Doing This:** Dependency rot is a major security risk. Dependabot automates the tedious process of checking for updates and creating PRs.

**Step-by-Step Instructions:**
1. Create a new file at `.github/dependabot.yml`.
2. Add the following configuration to tell Dependabot to check your npm packages weekly:
   ```yaml
   version: 2
   updates:
     - package-ecosystem: "npm"
       directory: "/"
       schedule:
         interval: "weekly"
   ```
3. Commit and push the file.
4. Go to the **Settings** tab on GitHub, click **Code security and analysis**, and ensure **Dependabot security updates** is enabled.
5. Dependabot will now automatically scan your `package.json` and open PRs to update vulnerable or outdated packages!

---
