## Lab 6: The Basics of Copilot Autocomplete (Ghost Text)
**Real-World Scenario:** You are writing a utility function to format currency. You want to see how Copilot speeds up boilerplate coding.
**Why we are doing this:** Understanding how to trigger, cycle through, and accept Copilot's "ghost text" predictions is the most fundamental AI coding skill.

### Step-by-Step Instructions:
1. **Create a New File:**
   * Create a file named `utils.js`.
2. **Start Typing:**
   * Type: `function formatCurrency(amount, currencyCode) {`
   * Pause and wait for 1-2 seconds.
3. **Interact with Ghost Text:**
   * Copilot will suggest the function body in gray "ghost text" (likely using `Intl.NumberFormat`).
   * **Do not press Tab yet.** Hover over the ghost text to see the Copilot toolbar.
   * Click the `>` arrow (or press `Alt+]` / `Option+]`) to cycle through alternative suggestions.
4. **Accept the Suggestion:**
   * Once you find a good suggestion, press `Tab` to accept the entire block.
   * *Explanation:* Copilot analyzes your function name and parameters to predict the most standard implementation.

---
