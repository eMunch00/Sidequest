# 🚀 NEW PROJECT STARTUP CHECKLIST

## STEP 1: Initialize Local Workspace
* **Open Terminal / Git Bash**
    * Navigate to your parent directory: `cd Documents/`
* **Create Project Folder**
    * `mkdir [PROJECT_NAME]`
* **Enter & Open in VS Code**
    * `cd [PROJECT_NAME]`
    * `code .`

## STEP 2: Launch the Local Ledger
* **Initialize Git**
    * `git init`
    * *Note: This creates the hidden .git "brain" for the folder.*
* **Configure Identity (If needed)**
    * `git config --global user.name "Your Name"`
    * `git config --global user.email "your@email.com"`
* **Set Primary Timeline**
    * `git branch -M main`
    * *Note: Ensures your local branch name matches GitHub's default.*

## STEP 3: Create GitHub Cloud Repository
* **Log in to GitHub.com**
* **Start New Repository**
    * Click the **"+"** icon (top right) -> **New repository**.
* **Configure Settings**
    * **Repository Name:** Match your local folder name.
    * **Public/Private:** Choose your visibility.
    * **Initialize this repository with:** Leave "README," ".gitignore," and "license" **UNCHECKED** (since we are linking an existing local folder).
* **Create Repository**
    * Click the green **Create repository** button.

## STEP 4: Link Local to Cloud
* **Copy Remote URL**
    * Copy the HTTPS link provided on the empty GitHub page.
* **Set the Remote Destination**
    * `git remote add origin [PASTE_URL]`
* **Perform Initial Sync**
    * `git add .`
    * `git commit -m "Initial setup: The foundation"`
    * `git push -u origin main`
    * *Note: The `-u` wires the folders together for future one-word "git push" commands.*

## STEP 5: Final Verification
* **Check Link Status**
    * `git remote -v`
    * *Check: Does the output show the correct URL for (fetch) and (push)?*
* **Verify Branch Connection**
    * `git branch -vv`
    * *Check: Does it show [origin/main]?*
* **Refresh GitHub Browser**
    * Ensure your files appear on the web dashboard.