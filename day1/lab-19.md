## Lab 19: Copilot - Generating Mock Data for Testing
**Real-World Scenario:** You are building a UI component that displays a list of products. The backend API isn't ready yet, so you need a realistic JSON array of mock products to test your frontend.
**Why we are doing this:** Creating realistic mock data manually is tedious. Copilot can generate large arrays of structured JSON data based on a single example or description.

### Step-by-Step Instructions:
1. **Create the File:**
   * Create `mockData.json`.
2. **Provide the Prompt/Example:**
   * Type the following:
     ```json
     [
       {
         "id": "PROD-001",
         "name": "Wireless Noise-Canceling Headphones",
         "price": 299.99,
         "category": "Electronics",
         "inStock": true
       },
     ```
3. **Let Copilot Generate:**
   * Press Enter and wait.
   * Copilot will generate `PROD-002`, `PROD-003`, etc., with realistic names, prices, and categories.
   * Press Tab to accept. Keep pressing Enter and Tab to generate more items until you have enough.
   * *Explanation:* Copilot recognized the JSON schema and the semantic context (Electronics) and generated matching dummy data.

---
