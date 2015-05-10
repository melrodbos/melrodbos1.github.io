# Reading JavaScript 
[(Mozilla Foundation - JavaScript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## Basics
 - JavaScript is **case-sensitive** and uses the **Unicode** character set. 
 - Instrucyions are called *statements* and are separasted by a semicolon.
 - Spaces, tabs and newline characters are called whitespace.
 - It is recommended to add semicolons at the end of your statements to avoid any "side effects"
 - Reference about JavaScript's [lexical grammar](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar) 

## Comments
 - The syntax of **comments** is as follows:
 
 
## Basic literal types 
 - `null.`: Special keyword denoting a null or empty value. It literally means no value. Intentionally empty.
 - `Boolean.`: `true` or `false`. It has exactly two values: true or false. Additional note: We can feed Boolean       numbers. If the numbers are greater than zero, the returned value will be ```True```. If the fed numbers are equal or less than zero, the returned value will be ```False```. (`Boolean` is a *Primitive* value) 
 - `Number.`: A numeric value. In ```JavaScript``` numbers can be written with or without decimals.
 - `String.`: Text. A sequence of characters that are written with quotes. We can use double quotes or single quotes. (Javascript does not care for double or sigle quotes)

## Special Constants
 - `Infinity`: Numeric value representing infinity. It has infinite values.
 - `NaN`: Not-a-Number. [A value that can not be represented.] (https://developer.mozilla.org/en-US/search?q=Nan+meaning)
 - `undefined`: Is a top level property whose value is [undefined] (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Grammar_and_types#Basics). 

## Basic Operators 

### Arithmetic
  - `+`: Unary plus operator. It attempts to convert the operand to a number, if it is not already.
  - `-`: Unary negation operator. Returns the negation of the operand.
  - `%`: Remainder. Binary operator. returns the integer remainder of dividing the two operands.
  - `++`: Unary operator. Adds one to its operand. If used as a prefix operator (++x), returns the value of its operand after adding one; if used as a postfix operator (x++), returns the value of its operand before adding one.
  - `--`: Unary operator. Subtracts one from its operand. 

### Comparison
 - `<`: Less than operator. Returns true if the left operand is less than the right operand.
 - `>`: Greater than operator. Returns true if the left operand is greater than the right operand.
 - `<=`: Less than or equal operator. Returns true if the left operand is less than or equal to the right operand.
 - `>=`: Greater than or equal operator. Returns true if the left operand is greater than or equal to the right operand.
 - `==`: Equal. Returns true if the operands are equal.
 - `!=`: Not equal. Returns true if the operands are not equal.
 - `!==`: Strict not equal. Returns true if the operands are not equal and/or not of the same type.
 - `===`: Strict equal. Returns true if the operands are equal and of the same type.

### Assignment
- *"An assignment operator assigns a value to its left operand based on the value of its right operand. The simple assignment operator is equal (=), which assigns the value of its right operand to its left operand. That is, x = y assigns the value of y to x."*
  - `=`: 
  - `+=`: 

### JavaScript Functions
*JavaScript functions are defined with the function keyword.* 
 - Example: Reference: (https://gist.github.com/2f0c3f39d0e5677395d3)
 ```
// function definition
function addition(a, b /* paramters go here */){
  // function body
  return a + b;
}
 
// function invocation
addition(3, 6 /* arguments go here */); // yields 9
addition(4, 7); // yields 11
addition(3, 18); // yields 21
```

### Typeof
*The typeof operator determines the type of a given object.*
- the `typeof` operator is followed by its operand.
- **Syntax**
 - type *operand*

- **Parameters**
 - operand is an expression representing the object or primitive whose type is to be returned.
- Examples:

 - *Numbers*
  - `typeof 37 === 'number';`
  - `typeof 3.14 === 'number';`
  - `typeof Math.LN2 === 'number';`
  - `typeof Infinity === 'number'`

## `Array`

. . .

### [Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Methods_2)

#### [`Array.prototype.pop`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)

* _params:_ none
* _returns:_ the last element
* _side-effects_: removes the element returned

##### Examples

### Length

### Array.prototype methods
- `[Array.prototype.pop()]` (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
*Removes the last element from an array and returns that element.*
- `[Array.prototype.splice()]` (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
*Adds and/or removes elements from an array.*
