# Python Notes

## BASH commands:
* `py` *opens REPL: Read Evaluate Print Loop environment*
    - `>>>` *text after ripple will be accessed by python interpreter*
* `quit ()` *leave REPL environment*

## pathlib: The Modern Way to Handle Files
**What it is** In the old days, developers treated file paths like `C:\Users\Documents\Spec.pdf` as plain text. This caused massive headaches because Windows uses backslashes (\) while almost every other system uses forward slashes (/). pathlib solves this by treating a path as a smart object that "knows" how to behave on any computer.
**How to use it**
Instead of messy string math, you use the / operator to join folders, which pathlib has cleverly redesigned to work for paths.

## Python Virtual Environment (venv)
**What it is** Think of your global Python installation as a massive communal workshop. A Virtual Environment is like renting a private locker inside that workshop. You can put exactly the tools (libraries) you need for your electrical estimation project inside that locker without worrying about someone else changing the version of a tool you rely on.
**How to set it up (Windows / VS Code)**
- Open your project folder in VS Code.
- Open the Terminal (Ctrl + or Terminal > New Terminal).
- Create the environment: Type the following and hit Enter:
    `python -m venv .venv`
    *(Note: .venv is the standard name, but you can name it anything.)*
- VS Code Integration: 
    VS Code will usually pop up a notification asking: "We noticed a new environment has been created. Do you want to select it for the workspace folder?" Click Yes.
**How to use it**
- Activation: In your terminal, run:
    `.venv\Scripts\activate`
    *(You’ll see (.venv) appear at the start of your command line prompt).*
- Installation: Now, when you run 
    `pip install google-generativeai` it installs only inside that folder.
**Usage with GeminiCLI:** Yes! If you are using a Python-based Gemini CLI tool, you simply activate your environment first, then run your CLI commands. This ensures the CLI uses the specific Python version and dependencies you’ve set aside for this project.