## Lab 3: Creating Your First GitHub Actions Workflow
**Scenario:** You want GitHub to automatically print a "Hello World" message every time code is pushed to the repository.
**Why We Are Doing This:** This introduces the YAML syntax and the basic architecture of GitHub Actions (events, jobs, and steps).

**Step-by-Step Instructions:**
1. In VS Code, create a new directory path: `.github/workflows/`
2. Inside that directory, create a file named `hello-world.yml`.
3. Use Copilot to help you write the workflow. Type this comment and press Enter:
   `// Write a GitHub Actions workflow that runs on push and echoes Hello World`
4. Accept Copilot's suggestion, which should look like this:
   ```yaml
   name: Hello World Workflow
   on: [push]
   jobs:
     greet:
       runs-on: ubuntu-latest
       steps:
         - name: Print Greeting
           run: echo "Hello World from GitHub Actions!"
   ```
5. Commit and push the file to GitHub.
6. Go to your repository on GitHub.com and click the **Actions** tab. You should see your workflow running (or already completed)! Click on it to view the logs.

---
