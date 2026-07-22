## Lab 18: Copilot for Writing Regular Expressions in CI

**Real-World Scenario:** You want to enforce a strict naming convention for your branches. A workflow should fail immediately if a developer pushes a branch that doesn't start with `feat/`, `bug/`, or `hotfix/`.

**Why We Are Doing This:** Regular Expressions (Regex) are notoriously difficult to write and read. Copilot can generate complex regex patterns instantly, making branch and commit validation much easier.

### Step-by-Step Instructions
1. Create a new workflow named `branch-lint.yml` that triggers `on: push`.
2. Open Copilot Chat and type: *"Write a bash step for GitHub Actions that checks the current branch name (`${{ github.ref_name }}`). Use a regular expression to ensure the branch starts with 'feat/', 'bug/', or 'hotfix/'. If it doesn't, exit with an error."*
3. Review the generated regex. It should look something like:
   ```bash
   if [[ ! "${{ github.ref_name }}" =~ ^(feat|bug|hotfix)/ ]]; then
     echo "Invalid branch name!"
     exit 1
   fi
   ```
4. Test it by pushing a branch named `test-branch` (it should fail) and then pushing `feat/login` (it should pass).

---
