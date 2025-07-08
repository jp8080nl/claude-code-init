# Initialize feature

Get details from the plan file in /project-management/plans/ $ARGUMENTS.

Follow these steps:

1. **Create a feature branch from develop**
   - Created feature branch from develop, named after GitHub issues (e.g., `feature/issue-123-add-login`)

2. **Write Tests First**
   - Write tests based on expected input/output pairs
      Write the tests as an 10x engineer!
   - Be explicit that you're doing TDD to avoid mock implementations
   - Do NOT create any implementation code at this stage
   - Run tests to confirm they fail initially

3. **Commit Tests**
   - Commit the tests once they accurately capture requirements
   - Tests serve as the specification for the implementation

4. **Check if we are ready to code**
   - Aks user if we are ready to to write code for the feature