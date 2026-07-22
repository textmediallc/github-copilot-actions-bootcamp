## Lab 1: Setting Up the Local Environment and Authenticating with GitHub
**Real-World Scenario:** Before any developer can contribute to a company's codebase, they must securely connect their local machine to the central repository.
**Why we are doing this:** Proper authentication prevents unauthorized access and ensures that all commits are accurately attributed to the correct developer, which is critical for auditing and collaboration.

### Step-by-Step Instructions:
1. **Open VS Code:** Launch Visual Studio Code on your local machine.
2. **Open the Terminal:** Go to `Terminal > New Terminal` (or press `` Ctrl+` ``).
3. **Configure Git Identity:**
   * Run: `git config --global user.name "Your First and Last Name"`
   * Run: `git config --global user.email "your.email@company.com"`
   * *Explanation:* This attaches your identity to every commit you make.
4. **Authenticate via GitHub CLI (gh):**
   * Run: `gh auth login`
   * Select `GitHub.com` (or your Enterprise Server).
   * Select `HTTPS` as your preferred protocol for Git operations.
   * Choose `Login with a web browser`.
   * Copy the one-time code provided in the terminal, press Enter to open your browser, paste the code, and authorize the application.
5. **Verify Authentication:**
   * Run: `gh auth status`
   * You should see a message confirming you are logged in.

---
