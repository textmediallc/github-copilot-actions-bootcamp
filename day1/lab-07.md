## Lab 7: Comment-Driven Development (CDD)
**Real-World Scenario:** You need to write a complex regex to validate company employee IDs, but you aren't a regex expert.
**Why we are doing this:** Writing clear comments forces you to define your intent before coding. Copilot translates this intent into accurate code, reducing syntax errors and saving time.

### Step-by-Step Instructions:
1. **Open your file:** Use `utils.js` from the previous lab.
2. **Write a Highly Specific Comment:**
   * Type the following exactly:
     ```javascript
     // Function to validate an employee ID.
     // Format: 2 uppercase letters, followed by a hyphen, followed by 5 digits.
     // Example valid: AB-12345
     // Example invalid: aB-1234, ABC-12345
     // Returns boolean.
     ```
3. **Trigger the Generation:**
   * Press `Enter` and start typing `function validate`.
   * Pause and wait for the ghost text.
4. **Review and Accept:**
   * Review the suggested regex (it should look like `/^[A-Z]{2}-\d{5}$/`).
   * Press `Tab` to accept.
   * *Explanation:* By providing constraints and examples in the comment, you prevented Copilot from guessing the format.

---
