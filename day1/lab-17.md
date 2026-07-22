## Lab 17: Copilot - Generating Documentation (JSDoc/Docstrings)
**Real-World Scenario:** You have written a complex function, and company policy requires JSDoc comments for all public methods so the documentation generator can parse them.
**Why we are doing this:** Writing documentation is often neglected because it's tedious. Copilot can read your code and generate accurate, perfectly formatted documentation blocks instantly.

### Step-by-Step Instructions:
1. **Create the Function:**
   * Create a file named `api.js` and add:
     ```javascript
     async function fetchUserData(userId, includeHistory = false) {
         if (!userId) throw new Error("User ID required");
         const url = `/api/users/${userId}?history=${includeHistory}`;
         const response = await fetch(url);
         if (!response.ok) throw new Error("Network error");
         return await response.json();
     }
     ```
2. **Trigger Documentation Generation:**
   * Place your cursor on the line immediately above the `async function` declaration.
   * Type `/**` and press Enter.
3. **Accept the JSDoc:**
   * Copilot will instantly generate the full JSDoc block, inferring the `@param` types (string/number, boolean) and the `@returns` type (Promise).
   * Press Tab to accept.
   * *Explanation:* Copilot analyzed the parameters, the default values, and the `await` keywords to build accurate documentation.

---
