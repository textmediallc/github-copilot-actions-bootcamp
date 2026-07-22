## Lab 10: Security and Context Management
**Real-World Scenario:** You need to write a database query, but you want to ensure Copilot doesn't suggest SQL injection vulnerabilities based on bad context.
**Why we are doing this:** Copilot learns from open files. If you have bad code open, it suggests bad code. Understanding how to manage context and prompt for security is critical for enterprise safety.

### Step-by-Step Instructions:
1. **Create Bad Context (The Trap):**
   * Create a file named `bad-examples.js` and add:
     ```javascript
     // Legacy query
     const getUser = (id) => db.query("SELECT * FROM users WHERE id = " + id);
     ```
   * Leave this file open in a background tab.
2. **Attempt to Write a New Query:**
   * Create `secure-db.js`.
   * Type: `// Function to get a post by ID`
   * Press Enter and type `const getPost = (id) =>`
   * *Observe:* Copilot will likely suggest another insecure, concatenated string query because it read `bad-examples.js`.
3. **Fix the Context (The Solution):**
   * Close `bad-examples.js`.
   * In `secure-db.js`, change your prompt to enforce security:
     ```javascript
     // Function to get a post by ID
     // SECURITY: MUST use parameterized queries to prevent SQL injection.
     const getPost = (id) =>
     ```
4. **Observe the Difference:**
   * Copilot should now suggest a secure implementation (e.g., using `?` or `$1` placeholders depending on the inferred library).
   * *Explanation:* Explicitly stating security constraints in your prompt overrides bad habits and forces the LLM to prioritize secure patterns.
