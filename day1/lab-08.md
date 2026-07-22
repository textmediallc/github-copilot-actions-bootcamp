## Lab 8: Using Copilot Chat for Code Explanation and Learning
**Real-World Scenario:** You've inherited a legacy codebase. You find a complex, uncommented data transformation function and need to understand it quickly before modifying it.
**Why we are doing this:** Reading code takes up to 70% of a developer's time. Copilot Chat acts as an instant senior developer to explain complex logic, reducing onboarding time.

### Step-by-Step Instructions:
1. **Create the Legacy Code:**
   * Create `legacy.js` and paste this confusing code:
     ```javascript
     const process = (d) => d.filter(x => x.v > 0).map(x => ({...x, v: x.v * 1.2})).reduce((a, c) => a + c.v, 0);
     ```
2. **Open Copilot Chat:**
   * Click the Chat icon in the Activity Bar (left side) or press `Ctrl+Cmd+I`.
3. **Ask for an Explanation:**
   * Highlight the code in `legacy.js`.
   * In the Chat input, type: `/explain What is this function doing step by step?`
4. **Review the Answer:**
   * Read the chat response. It will break down the `filter`, `map`, and `reduce` operations into plain English.
   * *Explanation:* The `/explain` slash command is a built-in shortcut that automatically grabs the highlighted context and formats the prompt for explanation.

---
