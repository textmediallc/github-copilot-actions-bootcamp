## Lab 20: Copilot - Exploring Alternative Implementations
**Real-World Scenario:** You wrote a function using a traditional `for` loop. A senior developer suggested it might be cleaner to use functional programming methods (like `map` or `reduce`), but you aren't sure how to rewrite it.
**Why we are doing this:** There are many ways to solve a problem in code. Copilot can show you alternative paradigms, helping you learn new syntax and improve code elegance.

### Step-by-Step Instructions:
1. **Create the Traditional Code:**
   * Create `loops.js` and add:
     ```javascript
     function getActiveUserNames(users) {
         let activeNames = [];
         for (let i = 0; i < users.length; i++) {
             if (users[i].isActive) {
                 activeNames.push(users[i].name.toUpperCase());
             }
         }
         return activeNames;
     }
     ```
2. **Ask for Alternatives:**
   * Highlight the function.
   * Open Copilot Chat and type: `Show me 2 alternative ways to write this function. One using functional array methods (filter/map), and one using a modern for...of loop.`
3. **Review and Compare:**
   * Review the chat output. Copilot will provide the `users.filter(...).map(...)` version and the `for (const user of users)` version.
   * *Explanation:* This turns Copilot into a teaching tool, allowing you to compare the readability and style of different programming paradigms side-by-side.
