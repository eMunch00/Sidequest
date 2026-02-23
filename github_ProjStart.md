[Link_back_to_Directory_Page](./README.md)
# 🚀 NEW PROJECT STARTUP CHECKLIST
![GitPS_Header](./Git_PS_Header.jpg)
## STEP 1: Initialize Local Workspace
* **Open Terminal / Git Bash**
    * Navigate to your parent directory: `cd Documents/`
* **Create Project Folder**
    * `mkdir [PROJECT_NAME]`
* **Enter & Open in VS Code**
    * `cd [PROJECT_NAME]`
    * `code .`
    * *Note: `code .` opens the project in a new VS Code window, within this window proceed to STEP 2*

## STEP 2: Launch the Local Ledger
* **Initialize Git**
    * `git init`
    * *Note: This creates the hidden .git "brain" for the folder.*
* **Configure Identity (If needed)**
    * `git config --global user.name "Your Name"`
    * `git config --global user.email "your@email.com"`
    * *verify values were recorded, run* `git config user.name && git config user.email`
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
    * **Initialize this repository with:** 
        * Leave "README" - *OFF*
        * Leave ".gitignore" - *NO*
        * Leave "license" *OFF* (we are linking an existing local folder).
* **Create Repository**
    * Click the green **Create repository** button.

## STEP 4: Link Local to Cloud
* **Copy Remote URL**
    * Copy the HTTPS link from **Quick Setup** pane on the empty GitHub page.
* **Set the Remote Destination**
    * `git remote add origin [PASTE_URL]`
* **Add README.md File**
    * `touch README.md` Creates a README file that will be landing page on GitHub
* **Open README.md File, copy the following text into it**
* *After pasting, fill out fields as noted*
    ``` 
    # 📁 [PROJECT NAME]
    > A brief, one-sentence "Elevator Pitch" describing the core purpose of this project.
    ---
    ## 🎯 Overview
    > Explain the "Why" behind this project. What problem does it solve, or what are you trying to learn by building it?

    ## 🚀 Features
    * **Feature 1:** Describe a key functionality.
    * **Feature 2:** Describe another functionality.
    * **Feature 3:** Mention a specific technical achievement.

    ## 🛠️ Tech Stack
    * **Version Control:** Git / GitHub
    * **Editor:** VS Code
    * **Languages/Tools:** [e.g., Markdown, JavaScript, Python]

    ## 📥 Installation & Setup
    1. **Clone the repo:**
    ```bash
    git clone [URL]```
   ```
* **Perform Initial Sync**
    * `git add .` stages contents of project and folders
    * `git commit -m "Origin Commit"` 
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