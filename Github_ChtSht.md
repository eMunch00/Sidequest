[Link_back_to_Directory_Page](./README.md)
# 🛡️ GIT & BASH CHEATSHEET
![GitCS_Header](./Git_CS_Header.jpg)
## 📂 General (Navigation & File Management)
*These can be used in any CMD Bash:*
* `pwd`
    * **Syntax:** "Print Working Directory." Displays the exact folder path where your terminal is currently standing.
* `ls -a`
    * **Syntax:** "List All." Shows all files and folders in the current directory, including hidden ones like the `.git` folder.
* `ls -R`
    * **Syntax:** "List Recursive." Displays every file in the current directory and all files within sub-directories.
* `cd [FOLDER_NAME]`
    * **Syntax:** "Change Directory." Moves the terminal focus into the specified folder. Use `cd ..` to move up one level.
* `mkdir [FOLDER_NAME]`
    * **Syntax:** "Make Directory." Creates a new folder with the specified name in your current location.
* `touch [FILE_NAME]`
    * **Syntax:** "Touch." Creates a new, empty file with the specified name and extension (e.g., `.md`).
* `mv [old_folder/file_name] [new_folder/folder_name]`
    * **Syntax:** "move." can be used to rename files or folders by targeting the current file/folder and specifying its desired name.
* `rm -r [FOLDER_NAME]`
    * **Syntax:** "Remove Recursive." Deletes a folder and everything inside it. **Note:** Use with caution.
* `rm -rf .git`
*Nuclear option, will delete you drive if not used properly*
    * **Syntax:** "Remove Recursive Force." Shreds the hidden Git ledger to "wipe the brain" of a project so you can start fresh.

## 🏗️ Category: Initiate (Project Setup)
* `git init`
    * **Syntax:** "Initialize." Creates the hidden `.git` vault in your folder, turning a standard folder into a version-controlled repository.
* `git remote add origin [URL]`
    * **Syntax:** "Remote Add." Saves the web address of your GitHub repository to your local ledger under the nickname "origin."
* `git branch -M main`
    * **Syntax:** "Branch Move." Forces the renaming of your primary local timeline to "main" to match GitHub's default convention.

## 📝 Commit (Save point on current branch)
*Commits cannot be deleted, only merged and squashed*
*Commits must be staged 'add' then committed 'commit -m'*
* `git status`
    * **Syntax:** "Status." Shows which files have been modified (Red), staged (Green), or are currently untracked by Git.
* `git add [FILE_NAME]`{Targeted stage of one file}
* `git add .` {stages all files & folders in current directory}
* `git add -A` {stages ALL files & folder in entire branch}
* **Syntax:** "Add." stages file to prepare for a commit.
* `git commit -m "[YOUR_MESSAGE]"`
    * **Syntax:** "Commit with Message." Permanently etches the staged changes into the local ledger with a descriptive note.
* `git log --oneline`
    * **Syntax:** "Log Oneline." Displays a condensed history of your commits, showing the 7-character Hash (Serial Number) and the message.
* `git checkout [COMMIT_HASH] [FILE_NAME]`
    * **Syntax:** "Checkout Commit." Temporarily restores a specific file to its state at the time of the provided Hash ID.

## 🌿Branches (Copy of project files for dev)
*Branches can be deleted after they have been merged*
*"Checkout -b Branch-Name" to create new branch*
*"Checkout Branch-Name" to move to exisitng branch*

* `git branch`
    * **Syntax:** "Branch." Lists all local timelines. The one with the asterisk (*) is where you are currently standing.
* `git checkout -b [NEW_BRANCH_NAME]`
    * **Syntax:** "Checkout New Branch." Creates a new branch and switches to it.
* `git checkout [BRANCH_NAME]`
    * **Syntax:** "Checkout." Switches your terminal and your physical files back to the specified existing branch.
* `git merge [SOURCE_BRANCH]`
    * **Syntax:** "Merge." Takes the history and files from the source branch and weaves them into the branch you are currently standing on.
* `git merge --squash [SOURCE_BRANCH]`
    * **Syntax:** "Squash Merge." Compresses all commits from the source branch into one commit on current timeline.
* `git branch -d [BRANCH_NAME]`
    * **Syntax:** "Delete Branch." Removes the branch "scaffolding" after it has been merged. Use `-D` to force delete unmerged branches.

## ☁️ Push & Pull (Up/Download with GitHub)
* `git push -u origin main`
    * **Syntax:** "Push Upstream." Uploads your local ledger to GitHub and "wires" the two together for the first time.
* `git push`
    * **Syntax:** "Push." Sends all new local commits to the connected GitHub repository after the initial setup is done.
* `git pull`
    * **Syntax:** "Pull." Fetches new data from GitHub and merges it into your local files. Used to keep your local machine in sync with the cloud.

## ⚠️ Undo & Emergency (Rollbacks)
*Use if local & remote ledgers are out of sync*
* `git reset --hard HEAD~1`
    * **Syntax:** "Hard Reset." The "Time Machine" that moves your timeline back by one commit and physically overwrites your current files. **Local only.**
* `git revert [COMMIT_HASH]`
    * **Syntax:** "Revert." Creates a brand-new "Patch" commit that performs the mathematical opposite of the specified mistake. **Use for Public/Pushed errors.**