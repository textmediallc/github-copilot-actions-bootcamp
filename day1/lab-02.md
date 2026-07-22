## Lab 2: Creating a Repository and Understanding the 3 Stages of Git
**Real-World Scenario:** You are starting a new microservice for the company's e-commerce platform. You need to initialize version control and make your first commit.
**Why we are doing this:** Understanding the Working Directory, Staging Area, and Repository is the foundation of Git. It prevents accidental commits of unfinished code or sensitive files.

### Step-by-Step Instructions:
1. **Initialize the Project:**
   * In the terminal, create a new folder: `mkdir ecommerce-inventory && cd ecommerce-inventory`
   * Initialize Git: `git init`
2. **Create the Initial Files (Working Directory):**
   * Create a file: `echo "# Inventory Service" > README.md`
   * Create another file: `echo "console.log('App starting');" > index.js`
   * Run: `git status`
   * *Explanation:* Both files are untracked in your Working Directory.
3. **Stage the Files (Staging Area):**
   * Run: `git add README.md`
   * Run: `git status`
   * *Explanation:* Only README.md is staged. This allows you to group related changes. Now stage the other file: `git add index.js`.
4. **Commit the Changes (Local Repository):**
   * Run: `git commit -m "Initial commit: Add README and basic index file"`
   * Run: `git log`
   * *Explanation:* The files are now safely stored in your local Git database with a snapshot of their current state.

---
