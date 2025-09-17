# Introduction to JavaScript

## The Basic Rules
- JavaScript is not a compiled language (the browser interprets it the same way it was written: as a human-readable sequence of Unicode characters)
- JavaScript interpreters parse the long strings of characters that make up a script and convert it into the following discrete input elements:
    - Tokens
    - Format control characters
    - Line terminators
    - Comments
    - Whitespace (almost always meaning tabs and spaces)
- The results of a script won't persist after reloading or navigating away unless you include explicit instructions to do otherwise
- At a high level, JavaScript applications are made up of *statements* and *expressions*

### Statements
- A statement is an instruction in code, written on one or more lines, that tells the computer to carry out a specific action.
- To be interpreted correctly, statements must end in a semicolon.
- Block Statements
    - A block statement uses braces `{}` to group several statements or declarations together and treat them as one combined unit.
    - (You will often see block statments alongside control flow statements, such as `if` )

### Expressions
- An expression is code that produces a value, which means it can be used anywhere a value is expected.
- Parentheses `()` can be used to group parts of an expression so they are calculated together, either to change the normal order of operations or to make the code easier to read.

### Weak Typing
- JavaScript is weakly typed, so you don’t have to declare data types explicitly; it figures out the type from context.
- Through *type coercion*, JavaScript automatically converts values between types (like turning numbers into strings when combined), and you can also convert them explicitly if needed.

### Case Sensitivity
- JavaScript is fully case sensitive, meaning that you must always capitalize everything consistently, from the roperties and methods build into the language to the identifiers you define yourself.

### Whitespace
- JavaScript is whitespace insensitive, meaning the interpreter ignores the amount and type (tabs or spaces) of whitespace used.
- Of course the presence of whitespace can be significant as a separator between lexical tokens (`let x`).