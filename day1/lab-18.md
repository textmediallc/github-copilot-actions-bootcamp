## Lab 18: Copilot - Fixing Bugs and Debugging
**Real-World Scenario:** You wrote a function to find the maximum value in an array, but it's returning the wrong answer or throwing an error. You can't spot the typo.
**Why we are doing this:** Copilot acts as a second pair of eyes. It can spot off-by-one errors, logical flaws, and syntax mistakes faster than manual debugging.

### Step-by-Step Instructions:
1. **Create the Buggy Code:**
   * Create `buggy.js` and add:
     ```javascript
     function findMax(arr) {
         let max = 0; // BUG: This fails if all numbers in array are negative
         for (let i = 1; i <= arr.length; i++) { // BUG: off-by-one error (<= instead of <)
             if (arr[i] > max) {
                 max = arr[i];
             }
         }
         return max;
     }
     ```
2. **Ask Copilot to Fix It:**
   * Highlight the function.
   * Open Copilot Chat and type: `/fix This function is returning incorrect results, especially for arrays with negative numbers. Find and fix the bugs.`
3. **Review the Fix:**
   * Copilot will explain the two bugs (initializing `max` to 0 instead of `arr[0]` or `-Infinity`, and the `i <= arr.length` bounds error) and provide the corrected code.
   * *Explanation:* Copilot identified edge cases (negative numbers) that the original developer missed.

---
