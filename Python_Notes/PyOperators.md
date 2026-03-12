# OPERATORS: Building blocks of Expressions

## Jargon: Expressions condense to values
expressions are evaluated into a value, typically a string ('true'/'false') or a value (0,1,2...)

## COMMON OPERATORS:
**Arithmetic Operators**
* `+` *Addition* - Adds two operands together to produce a sum.
* `-` *Subtraction* - Subtracts the right operand from the left operand.
* `*` *Multiplication* - Multiplies two operands to produce a product.
* `/` *Division* - Divides the left operand by the right operand and always returns a float.
* `%` *Modulus* - Returns the remainder of a division operation.
* `**` *Exponentiation* - Raises the left operand to the power of the right operand.

**Rounding & Floor Operators**
* `//` *Floor Division* - Divides operands and rounds down to the nearest whole number integer.
* `round()` *Rounding Function* - A built-in function that rounds a numeric expression to a specified number of decimals.

**Assignment Operators**
* `=` *Assignment* - Assigns the value of the right-hand expression to a left-hand variable.
* `+=` *Addition Assignment* - Adds a value to a variable and assigns the result back to that variable.
* `-=` *Subtraction Assignment* - Subtracts a value from a variable and assigns the result back to it.
* `*=` *Multiplication Assignment* - Multiplies a variable by a value and assigns the result back to it.

**Comparison Operators**
* `==` *Equal to* - Returns True if the values on both sides are equivalent.
* `!=` *Not equal to* - Returns True if the values on both sides are different.
* `>` *Greater than* - Returns True if the left operand is larger than the right.
* `<` *Less than* - Returns True if the left operand is smaller than the right.
* `>=` *Greater than or equal to* - Returns True if the left operand is greater than or equal to the right.
* `<=` *Less than or equal to* - Returns True if the left operand is less than or equal to the right.

**Boolean (Logical) Operators**
* `and` *Logical AND* - Returns True only if all expressions are true.
    *example*
    variable01 = True
    variable02 = True
    result = variable01 AND variable02
    *result = True*
* `or` *Logical OR* - Returns True if at least one of the expressions is true.
    *example*
    variable01 = True
    variable02 = False
    result = variable01 OR variable02
    *result = True*
* `not` *Logical NOT* - Inverts the Boolean value of the expression that follows it.
    *example*
    variable01 = False
    print("TextA" if not variable01 else "TextB")
    *result = TextA*
* `in` *Membership* - Returns True if a value is found within a sequence (like a list or string).
* `not in` *Negated Membership* - Returns True if a value is NOT found within a sequence.
    *example*
    variable_List = ["A", "B", "C"]
    "A" IN variable_list
    *result = True*
    "D" NOT IN variable_list
    *result = True*
* `is` *Identity* - Returns True if both variables point to the exact same object in memory.
* `is not` *Negated Identity* - Returns True if variables point to different objects in memory.
    *example*
    list_a = [1, 2, 3]
    list_b = [1, 2, 3]
    list_a == list_b    #are the values the same?
    *result = True*
    list_a is list_b    #are the variables the same?
    *result = False*
* `if else` *Ternary Operator* - Evaluates a condition and returns one of two values in a single expression line.
    *Example:* `print('textA' if 'conditional' else 'textB')`

**Not-So-Common Operators**
* `&` *Bitwise AND* - Compares bits of two integers and returns a 1 for each bit position where both are 1.
* `|` *Bitwise OR* - Compares bits and returns a 1 if at least one corresponding bit is 1.
* `^` *Bitwise XOR* - Returns a 1 only if exactly one of the corresponding bits is 1.
* `~` *Bitwise NOT* - Inverts all the bits of the operand (flips 0s to 1s and vice versa).
* `<<` *Left Shift* - Shifts the bits of the left operand to the left by the number of positions specified.
* `>>` *Right Shift* - Shifts the bits of the left operand to the right by the number of positions specified.
* `@` *Matrix Multiplication* - Performs matrix multiplication, specifically used with libraries like NumPy.
* `:=` *Walrus Operator* - Assigns a value to a variable as part of a larger expression.
* `%=` *Modulus Assignment* - Performs modulus and assigns the result to the variable in one step.
* `**=` *Exponent Assignment* - Raises the variable to a power and assigns the result back to it.