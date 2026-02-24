[Link_back_to_Directory_Page](./README.md)
# CMD BASH COMMANDS
![CMD_Header](CMD_Header.jpg)
* *The following are common commands for use in Bash Terminals*
## 📂 Directory: Contents
*These can be used in any CMD Bash:*
* `pwd`
    * **Syntax:** "Print Working Directory." Displays the exact folder path where your terminal is currently standing.
* `ls -a`
    * **Syntax:** "List All." Shows all files and folders in the current directory, including hidden ones like the `.git` folder.
    *Symbols displayed next to items in list*
    - `/`*Directory*	A standard folder.
    - `@`	*Link*	A shortcut pointing to a different address.
    - `*`	*Executable*  like a .exe or a script.
    - (none) *Regular File*	A standard file.
* `ls -R`
    * **Syntax:** "List Recursive." Displays every file in the current directory and all files within sub-directories.
## Directory: Navigation
* `cd [FOLDER_NAME]`
    **Syntax:** "Change Directory." Moves the terminal focus into the specified folder. Use `cd ..` to move up one level.
    - `Cd` change directory
    - `Cd /folder1/folder2` Moves to sub-folder1
    - `..` Moves up one tree
    - `../..`Moves up two trees
    - `../folder1`Moves up one folder then into sub-folder1
    - `.` References current folder, used for non-navigation commands.
    - `/` Root directory, parent tree of everything.
## Directory: Make
* `mkdir [FOLDER_NAME]`
    * **Syntax:** "Make Directory." Creates a new folder with the specified name in your current location.
    - `Mv [folder-name] /new-folder-path` *Move a folder from one directory to another*
    - `Mv [Folder-Name] [New-Folder-Name]` This will rename the targeted folder with  the new-folder-name.
    - `rmDir [Folder-Name]` = remove (delete) directory
## Files
* `touch [FILE_NAME]`
    * **Syntax:** "Touch." Creates a new, empty file with the specified name and extension (e.g., `.md`).
    - `Touch [FileName.type]` Make new file per designated name/type>
    - `Rm [file name]` Remove (delete) targeted file  
## Move/Delete/Rename: Files or Directories
* `mv [old_folder/file_name] [new_folder/folder_name]`
    * **Syntax:** "move." can be used to rename files or folders by targeting the current file/folder and specifying its desired name.
* `rm -r [FOLDER_NAME]`
    * **Syntax:** "Remove Recursive." Deletes a folder and everything inside it. **Note:** Use with caution.       
## Miscellaneous
    - `&&` <! Can be used to combine two commands into one line>
        ○ Example: `git add "FileName.md" && git commit -m "CommitName"              
## Nuxt, private server, development environment
    Npm run dev = run web application on private server for development review, NPM = Node Package Manager