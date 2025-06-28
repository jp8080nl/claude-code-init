When the /init command is called get the tech stack info from the PRD.md.

When the tech stack is clear implement test suite that works with GitHub status checks to run tests (continuous integration) 

# Test suite setup

## Tests
We will use the minimal effective test suite with only three layers:

1. Unit Tests (70%)
Exmplanation: 
- Test individual functions/methods in isolation
- Fast feedback, easy to debug
- Catch most bugs early

2. Integration Tests (20%)
Exmplanation: 
- Test component interactions and API contracts
- Verify data flow between systems
- Catch interface mismatches

3. E2E Tests (10%)
Exmplanation: 
- Test critical user paths only
- Verify the system works for real users
- Expensive to maintain, so keep minimal

## Setup

## Add Github workflow file and Scripts

### 1. Create Workflow File with tech stack in mind
Create `.github/workflows/ci.yml`:


### 2. Required package.json Scripts

## Run Github Check

1. Check with user if all GitHub settings are in place

# Note
Why this works:

Follows the testing pyramid - more cheap tests, fewer expensive ones
Unit tests catch bugs fastest and cheapest
Integration tests verify your architecture
E2E tests ensure business value delivery