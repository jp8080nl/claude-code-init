# GitHub Actions CI Setup - Compact Guide

## Free Tier Limits
- 2,000 minutes/month for private repos
- Unlimited for public repos
- Linux runners: 1x multiplier, Windows: 2x, macOS: 10x

## Quick Setup

### 1. Create Workflow File
Create `.github/workflows/ci.yml`:

```yaml
name: CI
on:
  push:
    branches: [main, develop]
  pull_request:
    branches: [main, develop]

jobs:
  test:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        node-version: [18, 20]
    steps:
      - uses: actions/checkout@v4
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: ${{ matrix.node-version }}
          cache: 'npm'
      - run: npm ci
      - run: npm run lint
      - run: npm test
      - run: npm run build
```

### 2. Required package.json Scripts
```json
{
  "scripts": {
    "test": "your-test-command",
    "lint": "your-lint-command", 
    "build": "your-build-command"
  }
}
```

### 3. Add Status Badge
Add to README.md:
```markdown
[![CI](https://github.com/username/repo/workflows/CI/badge.svg)](https://github.com/username/repo/actions)
```

## Advanced Features

### Test Coverage
```yaml
- run: npm test -- --coverage
- name: Upload coverage
  uses: codecov/codecov-action@v3
```

### Matrix Testing (Multiple OS)
```yaml
strategy:
  matrix:
    os: [ubuntu-latest, windows-latest, macos-latest]
    node-version: [18, 20]
runs-on: ${{ matrix.os }}
```

### Cache Dependencies
```yaml
- uses: actions/cache@v3
  with:
    path: ~/.npm
    key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
```

## Integration with Your TDD Workflow
- Automatically runs on feature branch pushes
- Blocks PR merges if tests fail
- Integrates with your `/2-feature-implement.md` and `/3-feature-pr-flow.md` commands

## Troubleshooting
- **Failed builds**: Check logs in Actions tab
- **Timeout**: Free tier has 6-hour job limit
- **Minutes exceeded**: Monitor usage in Settings > Billing

## Branch Protection Rules - Quick Setup

### Prerequisites
- Repository admin access
- Available on all GitHub plans (free included)

### Setup Steps

1. **Navigate to Settings**
   - Go to your repository → **Settings** → **Branches**

2. **Create Protection Rule**
   - Click **Add classic branch protection rule**
   - Enter branch name: `main` (repeat for `develop`)

3. **Essential Settings for CI**
   - ✅ **Require a pull request before merging**
     - Required approving reviews: `1`
     - ✅ Dismiss stale PR approvals when new commits are pushed
   - ✅ **Require status checks to pass before merging**
     - ✅ Require branches to be up to date before merging
     - *Note: CI workflow options appear after pushing workflow file*

4. **Additional Settings**
   - ✅ **Require conversation resolution before merging**
   - ✅ **Do not allow bypassing the above settings**

5. **Save**
   - Click **Create**

### Result
- PRs required for protected branches
- CI must pass before merge
- Prevents direct pushes to main/develop

That's it! Push the workflow file and your CI is active.