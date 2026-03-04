#TOML TEMPLATE
*TOML: Toms Obvious Minimal Language*
*The following is a template for use with GeminiCLI*

[commands]
# The 'dev' command: A full-lifecycle agentic workflow
dev = '''
1. **Environment Check**: Run `git status --short`. If there are any uncommitted changes, STOP and warn the user that they must commit or stash their work before I can proceed.
   !{git status --short}

2. **Branching**: If the repo is clean, generate a concise, kebab-case branch name based on the user's intent: "{{args}}". 
   Create and switch to that branch now.
   !{git checkout -b feature/{{args}}}

3. **Execution**: Now, proceed with the user's request: "{{args}}". Modify the necessary files in the project.

4. **Validation Loop**: 
   - Run the test suite using `npm test` (or the relevant test command).
   - If the tests fail, read the error output, refactor the code, and re-run the tests.
   - Repeat this up to 3 times. If it still fails, stop and report the logs.
   !{npm test}

5. **Completion**: Once tests pass, notify the user that the feature is ready and the code is verified.

6. **Handoff**: Ask the user: "Would you like me to spin up the Nuxt development server so you can preview these changes live?"
'''

