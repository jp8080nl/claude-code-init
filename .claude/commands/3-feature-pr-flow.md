# Git pull request flow

For the plan file in /project-management/plans/ $ARGUMENTS.
Get the GitHub issue number

Follow these steps:

1. **Create a pull request**
   - Create a pull request with:
     * Summary of changes and problem solved
     * Local checklist:
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

3. **Update the plan file and GitHub issue**
  - Update the the plan file in /project-management/plans/ $ARGUMENTS and mark everything as implemented
  - Move the plan file to /project-management/plans/implemented/
  - Use ‘gh issue’ close the GitHub issue as done