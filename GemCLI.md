# GEMINI CLI COMMANDS

## GENERAL USE
- `/exit` (or) `/quit` close gemini CLI
- `/` Will display a full list of commands
- `/help` will print the full list into command window with descriptions
- `/stats` shows weight (token count, massage count, file size) of current session.

## RAPID FIRE LIST FROM EX#4
- `/auth` command ... ???
- `/book` command ... ???
- `/clear` command, clears the Coversation List
- `/Copy` command, copies last response/output to the clipboard, usefull for pasting code into files.
- `/Docs` command, opens GemCLI docs in a browser ... use case?
- `/Directory` command, provide path to another directory for CLI to reference.
- `/Extensions` ... ???
- `/Model` *command*, allows user to change between CLI Models.
- `/Stats Model` *command/type* displays API & Token usage.
- `/Memory refresh` *command/type* directs CLI to rescan docs and commit to local memory (conversation list?)
- `/Memory add [...]` *command/type* allows user to add direction to overall Gemini.md file, for use across all CLI projects.
- `/Theme` *command* opens dialog to change the visual theme for CLI.
- `/Settings` *command* opens dialog box containing user/workspace/system settings.

## @DIRECTORY/FILE:
* when providing directions to GemCLI you can target these directions to a specific file by targeting the file with `@`
- `[direction] @[Path/file.name] *example syntax*
**Gemini CLI Companion** is extension app for VSCode. If enabled GeminiCLI will target any direction provided to the currently selected file. Further this app will direct GeminiCLI to selected code (highlited) within a file.


## LAUNCH GEMINI CLI IN NEW PROJECT
- `Gemini` will launch in bash.
- `/init` Create Gemini.md (markdown file) within a project. This can be used to provide project specific commands to GemCLI.
- `/memory refresh` makes Gemini CLI rescan any Gemini Files (md) to integrate any changes into its memory.


## /CHAT: SAVE, RESUME & COMPRESS- HOW GEMINI-CLI REMEMBERS CONTEXT
* GemCLI will create a .json file for every project, this is the 'Context Buffer' or 'Conversation List'. It contains a 'list' of every prompt/response with CLI. This list is ran with every new prompt entered into the Bash/Context window. This acts as CLI's memory.
**/CHAT - COMMANDS:**
- `/chat save [tag]` creates a 'savepoint' in a .json file per tag name, allowing any prompt data from this point to be removed from future prompts if initiated.
- `/chat resume [tag]` loads save point set at targeted tag name. This removes all context between the 'resume' command and 'save' command. Removing any direction or info from being 'remembered' in future prompts.
- `git resume` loads a terminal browser showing all saves, including auto saves with timestamps.
- `/compress` will compress the contents of the .json file to a summary of the current chat history. This minimizes token use for long branches.
- `/chat list` Provides a list of every save made.
**/CHAT - MANAGING 'LIST' WEIGHT & CONTEXT ROT**
* *Weight Affects Performance:*
    - *LATENCY*, how long it takes CLI to read context to start formulating a response.
    - *DRIFT*, as context grows instructions become less clear for CLI to follow. This will cause CLI to forget previous instructions.
    - *COST*, Paid API LLMs charge per token. 
* *Weight Parameters:* The weight of the Conversation Log will effect CLI's performance. 
    - *TOKEN COUNT*, Each word in the file is tokenized. 
    - *MESAGE COUNT*, each prompt/response is logged as a separate mesage. Each requires separate analysis (more messages more weight).- *FILE SIZE*, is the KB/MB size of .json 'Conversation Log'.
* *Best Practice for Weight Management*

## /CHAT & .GIT MANAGEMENT
* Upon starting a new project, start a new save point, this allows a restore point that does not contain any prompt context (like a main branch in github)
- `/chat save base-project` creates a new savepoint titled 'base-project'
    *set new savepoints in parallel with git-commits so context can be rolled back with code/file saves.* 
- `/chat resume base-project` restores save point 'base-project'.
    * resume to base-project (main branch) when starting a new git-branch, this starts the new developement branch with a fresh context window. 


