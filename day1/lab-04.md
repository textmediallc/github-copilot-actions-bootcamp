## Lab 4: Publishing to GitHub and Creating a Pull Request (PR)
**Real-World Scenario:** Your feature is complete locally. Now you need to push it to the company server and request a code review from your senior engineer.
**Why we are doing this:** Pull Requests are the primary mechanism for code review, quality assurance, and automated testing in modern development teams.

### Step-by-Step Instructions:
1. **Create the Remote Repository:**
   * Run: `gh repo create ecommerce-inventory --public --source=. --remote=origin --push`
   * *Explanation:* This creates the repo on GitHub.com and pushes your `main` branch.
2. **Push the Feature Branch:**
   * Run: `git checkout feature/db-connection`
   * Run: `git push -u origin feature/db-connection`
   * *Explanation:* The `-u` flag sets the upstream tracking branch.
3. **Create the Pull Request:**
   * Run: `gh pr create --title "Add database connection" --body "This PR adds the initial DB connection logic required for the inventory microservice."`
   * Select `Submit`.
4. **View the PR:**
   * Run: `gh pr view --web`
   * *Explanation:* This opens the PR in your browser. In a real scenario, your team would review the code here before merging.

---
