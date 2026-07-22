## Lab 19: Generating Workflow Documentation

**Real-World Scenario:** You have built a massive, complex CI/CD pipeline with multiple jobs, secrets, and reusable components. The DevOps team asks you to document how it works so junior developers can understand it.

**Why We Are Doing This:** Code isn't finished until it's documented. Copilot excels at reading complex YAML files and translating them into clear, human-readable Markdown documentation.

### Step-by-Step Instructions
1. Open your most complex workflow YAML file in VS Code.
2. Select all the text in the file (`Ctrl+A` or `Cmd+A`).
3. Open Copilot Chat and type: *"Create a `README.md` section documenting this GitHub Actions workflow. Include a table of the required Secrets, an explanation of the triggers, and a summary of what each job does."*
4. Review the generated Markdown.
5. Notice how Copilot perfectly extracted the secrets (e.g., `${{ secrets.NPM_TOKEN }}`) and formatted them into a neat table without you having to type a single word.
6. Save this documentation in your repository.
