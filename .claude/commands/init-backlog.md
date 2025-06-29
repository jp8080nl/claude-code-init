/init-backlog

Dependencies:
- Project is setup correctyle (check ./project-management/plans/project-setup.md) 

Add each feature as new GitHub issue

Instructions:
1. Read and analyze PRD.md from project-management/
2. Ultrathink and have a very deep understanding of the Project
3. Extract all features and requirements for the project
4. Break down into atomic, single-responsibility issues using this format:

   Title: [Component] Feature: <concise description>
   
   Body:
   ## User Story
   As a <user type>, I want <feature> so that <benefit>
   
   ## Acceptance Criteria
   - [ ] Specific measurable outcome 1
   - [ ] Specific measurable outcome 2
   
   ## Technical Notes
   - Implementation hints (if any)
   - Constraints or considerations
   
   ## Dependencies
   - Blocks: #<issue_number>
   - Blocked by: #<issue_number>
   
   Labels: [phase-X], [component], [priority], [size]

4. Ensure each issue is:
   - Completable in 1-3 days by one developer
   - Testable independently
   - Delivers user value (even if small)
   
5. Group issues by phase and component
6. Output as markdown with issue creation commands
