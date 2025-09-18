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
-   


## Symbols


## Variables