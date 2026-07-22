## Lab 14: Copilot - Generating Boilerplate and Scaffolding
**Real-World Scenario:** You are starting a new Express.js web server. Instead of looking up the documentation to remember how to set up the basic server structure, you want Copilot to write it for you.
**Why we are doing this:** Memorizing boilerplate code is a waste of mental energy. Copilot excels at scaffolding standard project structures, allowing you to focus on business logic immediately.

### Step-by-Step Instructions:
1. **Create the File:**
   * Create a file named `server.js`.
2. **Prompt for Boilerplate:**
   * At the top of the file, write this comment:
     ```javascript
     // Set up a basic Express server
     // Import express, define port 3000
     // Add a GET route for '/' that returns "Hello World"
     // Start the server and log the port
     ```
3. **Generate:**
   * Press Enter and wait.
   * Copilot should generate the `require('express')`, the app initialization, the route, and the `app.listen` block.
4. **Accept and Review:**
   * Press Tab to accept.
   * *Explanation:* By providing a clear, structured list of requirements, Copilot generated the entire file perfectly in seconds.

---
