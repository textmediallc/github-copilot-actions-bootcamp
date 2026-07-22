## Lab 16: Copilot - Explaining Regular Expressions
**Real-World Scenario:** You find a massive, cryptic regular expression in the codebase used for validating email addresses. You need to modify it to allow a new top-level domain, but you don't understand how it currently works.
**Why we are doing this:** Regex is notoriously difficult to read. Copilot can break down complex regex patterns into plain English, making them maintainable.

### Step-by-Step Instructions:
1. **Create the Regex:**
   * In a new file, paste this line:
     `const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$/;`
2. **Ask for Explanation:**
   * Highlight the regex.
   * Open Copilot Chat and type: `/explain Break down exactly what this regular expression is doing.`
3. **Review the Breakdown:**
   * Read the chat response. It will explain the `^` (start of string), the character classes `[a-zA-Z0-9._%+-]`, the `@` symbol, the domain part, and the `$` (end of string).
   * *Explanation:* You now understand the regex well enough to modify the `{2,}` part if you needed to restrict the top-level domain length.

---
