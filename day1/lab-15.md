## Lab 15: Copilot - Translating Code Between Languages
**Real-World Scenario:** Your company is migrating a critical microservice from Python to JavaScript (Node.js). You need to translate several complex utility functions.
**Why we are doing this:** Copilot is polyglot. It understands the syntax and idioms of dozens of languages and can accurately translate logic, saving hours of manual rewriting.

### Step-by-Step Instructions:
1. **Create the Source Code:**
   * Create a file named `math_utils.py` and paste this Python code:
     ```python
     def calculate_factorial(n):
         if n < 0:
             return None
         if n == 0 or n == 1:
             return 1
         result = 1
         for i in range(2, n + 1):
             result *= i
         return result
     ```
2. **Translate via Chat:**
   * Highlight the Python code.
   * Open Copilot Chat and type: `Translate this Python function into modern JavaScript.`
3. **Review the Output:**
   * Copilot will generate the equivalent JS code.
   * *Explanation:* Notice that it doesn't just do a literal translation; it adapts the code to JavaScript idioms (e.g., using `let` instead of Python's implicit scoping).

---
