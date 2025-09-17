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


## Booleans


## Null and Undefined Values


## BigInt


## Symbols


## Variables