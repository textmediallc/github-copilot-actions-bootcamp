## Lab 9: Refactoring and Generating Tests with Copilot Chat
**Real-World Scenario:** The legacy code from Lab 8 works, but it's unreadable and has no tests. Company policy requires all new code to be tested and readable.
**Why we are doing this:** Copilot excels at transforming existing logic into better patterns (refactoring) and generating boilerplate unit tests, ensuring code quality without manual drudgery.

### Step-by-Step Instructions:
1. **Refactor for Readability:**
   * Highlight the code in `legacy.js`.
   * In Copilot Chat, type: `Refactor this code to be more readable. Give the variables descriptive names assuming 'd' is an array of 'transactions' and 'v' is 'value'. Use modern ES6 syntax.`
   * Click the `Apply in Editor` button (the double-arrow icon) on the generated code block to replace the old code.
2. **Generate Unit Tests:**
   * Highlight the newly refactored code.
   * In Copilot Chat, type: `/tests Generate Jest unit tests for this function. Include cases for empty arrays, negative values, and normal transactions.`
3. **Review the Tests:**
   * Copilot will generate a `describe` block with multiple `it` statements.
   * *Explanation:* You've just improved code quality and test coverage in minutes, a task that normally takes significant manual effort.

---
