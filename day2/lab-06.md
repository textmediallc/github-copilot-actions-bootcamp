## Lab 6: Storing and Using Encrypted Secrets
**Scenario:** Your deployment script requires an API key, but you cannot hardcode it in your YAML file because it would be visible to anyone who views the repository.
**Why We Are Doing This:** Security is critical. GitHub Secrets allow you to securely pass sensitive data to your workflows without exposing it in the codebase.

**Step-by-Step Instructions:**
1. Go to your repository on GitHub.com.
2. Click **Settings** > **Secrets and variables** (in the left sidebar) > **Actions**.
3. Click the **New repository secret** button.
4. Name: `MY_SUPER_SECRET_API_KEY`
5. Value: `12345-ABCDE-SECRET`
6. Click **Add secret**.
7. In your workflow YAML, add a step that uses the secret:
   ```yaml
       - name: Use Secret
         env:
           API_KEY: ${{ secrets.MY_SUPER_SECRET_API_KEY }}
         run: echo "Deploying with key... (key is masked in logs)"
   ```

---
