# Data Types and Structures

Primitives are the most basic data type in JavaScript and there are 7 different types:
- Numbers
- Strings
- Booleans
- `null`
- `undefined`
- BigInt
- Symbol

Primitive values are immutable, meaning the value itself cannot be altered (for example `true` with always mean true, and `5` will always mean 5).

The other data type in JavaScript is objects. Objects are mutable and stored by reference. Examples of objects are:
- Arrays
- Functions
- Dates
- Custom Objects

Variables are containers that store values of any data type. Variables that store primitives can be reassigned, but the literal values themselves never change.

## Numbers
- A number value is any sequence of digits representing a numeric value.
- The number type in JavaScript also includes special values:
    - `Inifinity` -> represents values beyond the largest possible number.
    - `NaN` -> ('Not a Number') shows up when you try to do math on something that isn't a valid number.

### The Number Object
- When a value is passed to the `Number()` function, that value is converted to the number equivalent.
- Passing a `false` or `null` value to `Number()` returns `0`, and `true` returns `1`.
- If a value can't be converted, as in the case of `undefined` or a string containing non-numeric characters, the `Number` function returns `NaN`.
- Using the `Number` object as a constructor creates a `Number` object rather than a number literal; while it behaves like its value in mathematical operations, it fails strict equality (===) comparisons with literals because the data types don’t match.

### Floats and Integers
- JavaScript has only one number type: 64-bit double precision floating-point (IEEE 754 standard).
- All numbers are stored as binary floating-point values (floats), which can lead to precision errors.
- Integers are also stored as floats, but values between -(2^53 - 1) and 2^53 - 1 can be represented exactly.
- It is recommended to use whole numbers whenever possible to minimize floating-poinmt precision issues.

### Number Operators
- When you use standard mathematical operators with number primitives, the mathematical  order of operations applies.
- You can also use mathematical assignment operators to perform a mathematical oepration on the value of a varibale and immediately assign that newly-calculated value to the variable.

### Symbolic Values
 - Special number cases in JavaScript:
    - `NaN`
        - Returned when a mathematical operation cannot produce a valid number.
        - `NaN` is case-sensitive
    - `Infinity` and `-Infinity`
        - Returned when dividing by zero
        - It's case-sensitive: `Infinity` works, but `infinity` is not defined.

## Strings
- Any set of characters —letters, numbers, symbols, and so on— between a set of either double quotation marks (`"`), single quotation marks (`'`), or backticks (`) is a string primtive.
- A string literal is the written representation of a string primitive in code, created by enclosing characters in quotation marks.
- In other words: a string literal is the syntax, while a string primitive is the actual value stored in memory, and a string object is the object wrapper around a string primitive.

### String Object
- When called as a function, the `String` object coerces a specified value to a string literal.

### Concatentation
- When used in the context of string instead of numbers, a single plus sign (`+`) acts as a concatenation operator, combining multiple string values into a single string.

### String Literals and Template Literals
- Single quotes, double quotes, and backticks can be used interchangeably for creating string primitives.
- You can also use backticks to specify *template literals* which allow for multi-line strings and string interpolation.
- Tempalte literals can contain placeholder expressions marked by a dollar sign and curly braces (`${}`).
- These placeholders are 'interpolated' by default, meaning that the result of the expression replaces the placeholder in the final string.

## Booleans
- The boolean primitive is a logical data type with only two values: `true` and `false`.
- Values that result in `false` include `0`, `null`, `undefined`, `NaN`, and empty string (`""`), an ommitted values, and a `false` boolean. All other values result in `true`.
- Avoid using the `Boolean` object as a constructor as it creates an object instead of a simple true/false value —and that object will always act like `true` even if it contains `false`.


## Null and Undefined Values
- Javascript has multiple ways of indicating the absence of a value; the two most common being the `null` and `undefined` data types.
- In the strictest sense, `null` represents a value intentionally defined as 'blank', and `undefined` represents a lack of any assigned value.

### null
- The `null` keyword represents an intentionally defined absense of value.
- `null` is a primitive, although the `typeof` operator returns that `null` is an object. (This is a error that has been around since the first version of JavaScript)

### undefined
- `undefined` is a primitive value assigned to variables that have just been declared, or to the resulting value of an operation that doesn't return a meaningful value.


## BigInt
- Numbers in JavaScript can only safely handle integers up to a certain size and if you go beyond that, JavaScript with start rounding your numbers, and you lose accuracy.
- BigInt primitives allow mathematical operations on numbers outside the range allowed by `Number` without losing precision.
- To create a BigInt, append `n` to the end of a number literal, or pass an integer or numeric string value to the `BitInt()` function.
- BigInt cannot be mized with normal Numbers in math operations and are not compatible with `Math` object methods (but you can still do basic operations).


## Symbols
- A Symbol is a special primitive in JavaScript that always creates a unique value, even if it has the same description as another symbol. Unlike strings, which can be equal if they contain the same characters, symbols are never equal to each other. They are often used as unique keys in objects to avoid naming conflicts.
- You can add an optional description when creating a symbol, but it only helps with debugging and does not change the uniqueness. Symbols can be regular symbols made with `Symbol()`, shared symbols from the global registry using `Symbol.for()`, or built-in well-known symbols like `Symbol.iterator`.
- Symbols cannot be created with `new Symbol()` and are not included in normal object loops. If you want to see them, you need to use `Object.getOwnPropertySymbols()`.

### Shared Symbols
- `Symbol.for(key)` looks in the global symbol registry; if the key exists, it returns that symbol, otherwise it creates one.
- Registry symbols are shared across code, unlike normal `Symbol()` values which are always unique.
- Use `Symbol.keyFor(symbol)` to get the key string of a registry symbol.

### "Well-Known" Symbols
- Well-known symbols are static properties of the `Symbol` object and provide unique property keys for accessing and modifying JavaScript's built-in methods, while preventing core behavior from being unintentionally overwritten.
- Well-known symbol values are often stylized with a `@@` prefix or wrapped in `%` to differentiate their keys from their mutable prototypes.

## Variables
- Variables are a data structure that assigns a representative name to a value and they contain data of any kind.
- A variable's name is called an identifier. A valid identifier must follow these rules:
    - Identifiers can contain Unicode letters, dollar signs ($), underscores (_), digits (0-9), and even some Unicode characters.
    - Identifiers can't contain whitespace, because the parser uses whitespace to separate input elements.
    - Identifiers must start with a letter, underscore (_), or dollar sign ($). They can't start with digits, to prevent confusion between numbers and identifiers.
- camelCase is a very common connvention for identifiers made up of multiple words.
- JavaScript doesn't give any special privilege or meaning to identifiers that begin with underscore characters, but they're typically used to show that a variable, method, or property is "private", meaning that it's only inteded for use within the context of the object that contains it, and shouldn't be accessed or modified outside that context.

### Variable Declaration
- A variable is declared using the `let`, `const`, or `var` keywords.
- Use `let` or `var` to declare a variable that can be changed at any time. (`let` is better for modern codebases/browsers)
- A declared variable is initialized by assigning a value to the variable. Use a single equals sign (`=`) to assign or resassign a value to a variable.
- If you don't initialize the variable right away, the initial value is `undefined` until your code assigns it a value. (A variable with an `undefined` value is different from an undefined variable whose identifier hasn't been declared yet.)
- A variable;s connection to a value is called a binding and a binding list lets you declare multiple variables in one statement.
- Reassigning a value uses `=` only, not `let` or `var`, and variables can be resassigned using their current value.

### const
- Use the `const` keyword to declare a constat, a type of variable that must be immediately initialized, and then can't be changed.
- If you try to declare a constant without initializing it, you get a syntax error.
- Trying to change the value of a variable declared with `const` causes a type error, but when a constant is associated with an object, the properties of that object can be altered.
- A constant that contains an object is an immutable reference to a mutable data value. While the constant itself can't be changed, the properties of the referenced object can be altered, added to, or removed.

### Variable Scope
- A variable's scope is the part of a script where that variable is available and outside that scope, it won't be defined. (Not as an identifier containing an `undefined` value, but as if it hadn't been declared.)
- You can scope variables to block statements (block scope), individual functions (function scope), or the entire JavaScript application (global scope).

#### Block Scope
- Variables declared with `let` or `const` are block scoped, meaning they only exist inside th `{ }` block where they are declared. (Trying to use them outside this gives a ReferenceError).
- You can reuse the same identifier inside different blocks without conflict, because each block has its own scope.
- Parent block variables are accessible in child blocks and child blocks can modify parent variables, unless a enw variable with the same name is declared inside the child block.

#### Function Scope
- Variables declared with `var` are function scoped, meaning they only exist inside the function where they are declared. (Trying to do so will result in a ReferenceError).
- Even after the function is called and the variable is created, it still disappears once the function ends and cannot be used outside.

#### Global Scope
- A global variable is available everywhere in a JavaScript program —inside any block, function, or script on the page. (Can be declared with `var`, `let`, or `const`).
- While convenient, global variables are risky because any part of the code (including third-party libraries) can change them.

#### Variable Hoisting
- Hoisting means JavaScript moves variable and function declarations to the top of their scope before running the code.
- `var` variables are hoisted and initialized as `undefined` while `let` and `const` are hoisted but live in a temporal dead zone (TDZ) until declared.     
    - Accessing them before declaration throws a ReferenceError. This error is different from the error you might expect when trying to access an undeclared variable.
    - Because JavaScript has hoisted the variable, it's aware that the variable will be created within the given scope. However, instead of making that variable available before its declaration with a value of undefined, the interpretor throws an error.