/new-github-issue 

Ultra think on new github issue: $ARGUMENTS.

Instructions:
1. Aanalyze the feature or bug though the $ARGUMENTS
2. Ask questions if the feature is no clear or ask the user to label it as unrefined
3. Break down into atomic, single-responsibility issue with format:

   Title: [Component] - <concise description>
   
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

5. Use ‘gh issue create’ to create issues
   
6. Output as markdown with issue creation commands
