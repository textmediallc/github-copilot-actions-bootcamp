## Lab 14: Matrix Builds for Cross-Platform Testing

**Real-World Scenario:** Your team is building a CLI tool using Node.js. Because developers will run it on Mac, Windows, and Linux, you need to guarantee the tests pass on all three operating systems simultaneously.

**Why We Are Doing This:** Matrix builds are one of the most powerful features of GitHub Actions. They allow you to multiply a single job into dozens of parallel jobs with just three lines of code.

### Step-by-Step Instructions
1. Open your CI workflow file.
2. In your build job, under the `runs-on:` key, add a strategy matrix.
3. Open Copilot Chat and type: *"Update this GitHub Actions job to use a matrix strategy. It should test across three operating systems (ubuntu-latest, windows-latest, macos-latest) and two Node versions (18, 20)."*
4. Apply the changes. Your YAML should now look like:
   ```yaml
   strategy:
     matrix:
       os: [ubuntu-latest, windows-latest, macos-latest]
       node-version: [18, 20]
   runs-on: ${{ matrix.os }}
   ```
5. Commit and push. Look at the Actions tab—you should see 6 parallel jobs running at once!

---
