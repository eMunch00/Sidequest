# PYTHON VARIABLES:

## Jargon:
variables are initialize by binding (storing) an expression to it

## Syntax:
`[variable] = '[expression]'` with the '=' statement, we are assigning the 'variable' the context held within the 'expression'
    *the value must be in quotes*
    *Variable cannot contain `!`, `-`, or start with numbers, or contain other key words (commands)*

## Statements V. Expressions:
**Statements are Actions** represent an action or a command that the python interpreter carries out. The use of a variable is a statement, specifically an assignment statement.
    **Common Statements by Category and their action**
    1. `=` *Assignment* Binds an expression to a name (identifier).
    2. `if / elif / else` *Conditional* Branches execution based on a Boolean expression.
    3. `for` *Iteration* Iterates over a sequence (like a list or string).
    4. `while` *Iteration* Repeats a block as long as a condition is True.
    5. `def` *Definition* Defines a reusable function block.
    6. `return` *Control Flow* Exits a function and passes a value back to the caller.
    7. `import` *Module* Accesses code from other files or the Python Standard Library.
    8. `try / except` *Error Handling* Traps Exceptions so your script doesn't crash.
    9. `print()` *Expression-Statement* Technically a function call, but used as a standalone statement to output data."
    10. `with` *Context Manager*Safely manages external resources like files (crucial for Windows).
**Expressions are Data** are any combination of values, variables, and operators that the Python interpreter evaluates to produce a single value. If you can print it or assign it to a variable, it’s an expression.
*Examples:*
    - `5 + 5` would produce `10` (or) 
    - `"Gemini" + "CLI"` would produce `GeminiCLI`. 
    python will compute these expressions into a single data block.

## Expressions & Statement Combinations:
**Statements with Expression** 
    *Example:* Most common composition of code, is a variable. 
    - `Variable = 'Expression'` 
    'variable =' is the statement with the 'expression' being assigned to it.
**Compound Statement** is a statement within a statement.
    *Example:* The following statement contains two statements:
    ```Python
    if True:
        print("The condition is met.")
        x = 100```
    'if True' being the primary conditional statement, then 'Print(text)' and assign 'x = 100'.
**Nesting** Expressions within Expressions.
    *Example:* the following expression contains two other expressions: 
    `(10 + 5) * (20 / 4)`
    '(10 +5)' is an expression, '(20 / 4)' is another expression, both are 'nested' in the same expression.
**Syntax Error** You cannot 'nest' a Statement within an Expression.
    *Example:* the following trys to insert a 'variable' statement into a 'print' statement (where an expression should be)
    `print(user_name = "Dev")`
    Python will stop compiling at this point and return an error.
