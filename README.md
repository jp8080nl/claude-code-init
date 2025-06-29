## How to use this repo (You could also fork of course)

**clone init files and push to you own repo**
    1. Clone this public repo to you project folder
    git clone https://github.com/jp8080nl/claude-code-init.git .
    2. Remove the original remote
    git remote remove origin
    3. Add your private repo as the new origin
    git remote add origin https://github.com/yourusername/your-private-repo.git
    4. Push to your private repo
    git push -u origin main
    5. Change remote url
    git remote set-url origin https://github.com/yourusername/your-private-repo.git

**Create a development branch and make it default**
    git checkout -b develop
    git push -u origin develop
    Make the develop branch the default. Her is how:
    1. Go to your repository on GitHub: https://github.com/jp8080nl/shopify-translate-engine
    2. Click on "Settings" tab
    4. In the "Default branch" section, click the switch icon (⇄)
    5. Select "develop" from the dropdown
    6. Click "Update" to confirm the change
    7. GitHub will ask you to confirm - click "I understand, update the default branch"

**Setup automated test (CI)**
    1. Navigate to Settings
    - Go to your repository → **Settings** → **Branches**
    2. Create Protection Rule
    - Click **Add classic branch protection rule**
    - Enter branch name: `main` (repeat for `develop`)
    3. Essential Settings for CI
    - ✅ **Require a pull request before merging**
        - Required approving reviews: `1`
        - ✅ Dismiss stale PR approvals when new commits are pushed
    - ✅ **Require status checks to pass before merging**
        - ✅ Require branches to be up to date before merging
        - *Note: CI workflow options appear after pushing workflow file*
    4. Additional Settings
    - ✅ **Require conversation resolution before merging**
    - ✅ **Do not allow bypassing the above settings**
    5. Save
    - Click **Create**

6. Add your prd
Add your PRD.md file to the project-management folder

x. Remove this README.md content and replace with your own
