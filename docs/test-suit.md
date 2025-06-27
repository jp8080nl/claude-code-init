The minimal effective test suite needs just three layers:
1. Unit Tests (70%)

Test individual functions/methods in isolation
Fast feedback, easy to debug
Catch most bugs early

2. Integration Tests (20%)

Test component interactions and API contracts
Verify data flow between systems
Catch interface mismatches

3. E2E Tests (10%)

Test critical user paths only
Verify the system works for real users
Expensive to maintain, so keep minimal

Why this works:

Follows the testing pyramid - more cheap tests, fewer expensive ones
Unit tests catch bugs fastest and cheapest
Integration tests verify your architecture
E2E tests ensure business value delivery