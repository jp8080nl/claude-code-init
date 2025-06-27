# Git pull request flow

1. **Create a pull request**
   - Create a pull request with:
     * Summary of changes and problem solved
     * Checklist:
       □ Tests written and passing
       □ Code coverage maintained/improved
       □ Documentation updated
       □ Linting/formatting complete
       □ CHANGELOG updated (if applicable)

2. **Check automated tests and do PR review**
   - Check if GitHub automates tests and provide info on failures
   - Ask user to review PR and to provide feedback if needed
   - If changes are requested: return to step 1 in Implement or update Feature and repeat the process
   - If PR is accepted ask user to merge feature to development branch
   - Ask user to delete the feature branch