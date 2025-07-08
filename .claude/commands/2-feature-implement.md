# Implement or update Feature

Get details from the plan file in /project-management/plans/ $ARGUMENTS.

Follow these steps:

1. **Implement Code and update documentation**
   - Write code to pass the tests WITHOUT modifying the tests
      Write code like a 10x engineer - less code the better!
   - Update relevant documentation as you code:
     * API docs for new endpoints
     * README for new features or setup changes
     * Code comments for complex logic
     * CHANGELOG.md for user-facing changes
   - Iterate: write code → run tests → adjust code → repeat
   - Continue until all tests pass

2. **Run Puppeteer test when UI changes**
   - Use puppeteer via MCP to test the changes if you have made changes to the UI

3. **Run Linting and Formatting**
   - Run automated formatter 
   - Run linter to catch potential bugs

4. **Check code coverage**
   - Run Code coverage tests only on files we changed

5. **Commit and push**
   - Commit and push the code once all tests pass and you're satisfied with the implementation. Ideally, each commit and push contains an isolated, complete change.

6. **Check if we are ready to start the PR flow**
    - Ask user if we are ready to start the PR flow for the coded feature