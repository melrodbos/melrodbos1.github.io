# Reading JavaScript 
[(Mozilla Foundation - JavaScript)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## Basics
 - JavaScript is **case-sensitive** and uses the **Unicode** character set. 
 - Instrucyions are called *statements* and are separasted by a semicolon.
 - Spaces, tabs and newline characters are called whitespace.
 - It is recommended to add semicolons at the end of your statements to avoid any "side effects"
 - Reference about JavaScript's [lexical grammar](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar) 

### Comments
 - The syntax of **comments** is as follows:
 ```
// a one line comment
 
/* this is a longer, 
   multi-line comment
 */
 
/* You can't, however, /* nest comments */ SyntaxError */
```

### Declarations
 - There are three kinds of declarations in JavaScript.
 ```
*var*
Declares a variable, optionally initializing it to a value.

*let*
Declares a block scope local variable, optionally initializing it to a value.

*const*
Declares a read-only named constant.
 ```

#### Variables
 - We use variables as symbolic names for values in your application.
 - The name of the viariables are callled **identifiers**
 - A JavaScript identifier must start with:
  - a letter 
  - underscore `_`
  - dollar sign `$`
  - subsequent characters can also be digits `0-9` 
 - Because JavaScript is case sensitive, letters include the characters "A" through "Z" (uppercase) and the characters "a" through "z" (lowercase). 

#### Evaluating variables
 - A variable declared using the `var` or `let` statement with no initial value specified has the value `undefined`.
  - Examples:
  
   - You can use undefined to determine whether a variable has a value. 
   - In the following code, the variable input is not assigned a value, and the `if` statement evaluates to true.
```
var input;
if(input === undefined){
  doThis();
} else {
  doThat();
}
```
   - The undefined value behaves as false when used in a boolean context. For example, the following code executes the function myFunction because the myArray element is `undefined``:
```
var myArray = [];
if (!myArray[0]) myFunction();
```
   - The undefined value converts to `NaN` when used in numeric context.
```
var a;
a + 2 = NaN
```
   - When you evaluate a `null` variable, the `null` value behaves as 0 in numeric contexts and as false in `boolean` contexts. For example:
```
var n = null;
console.log(n * 32); // Will log 0 to the console
```
## Data structures and types
###Data types
 - There are seven data types: 
  - **Six** are *primitives*:  
   - Boolean: `true` and `false`
   - null: A keyword denoting a null value
   - undefined: A top-level property whose value is undefined
   - Number: 1 or 2.34567
   - String: "How you doin'"
   - Symbol: A data type whose instances are unique and immutable
 - and Object
 
### Basic literal types 
 - `null.`: Special keyword denoting a `null` or empty value. 
  - It literally means no value. 
  - Intentionally empty.
 - `Boolean.`: `true` or `false`. It has exactly two values: `true` or `false`. 
  - **Note: We can feed Boolean numbers**. 
  - If the numbers are greater than zero, the returned value will be ```True```. 
  - If the fed numbers are equal or less than zero, the returned value will be ```False```. 
  - (`Boolean` is a *Primitive* value) 
 - `Number.`: A numeric value. 
  - In ```JavaScript``` numbers can be written with or without decimals.
 - `String.`: Text. 
  - A sequence of characters that are written with quotes. 
  - We can use double quotes or single quotes. 
  - (Javascript does not care for double or sigle quotes)

### Special Constants
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

## JavaScript Functions
*JavaScript functions are defined with the `function` keyword.* 
 - Example: [Reference](https://gist.github.com/2f0c3f39d0e5677395d3)
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

//String Calculator example:

//function definition
function plus(A, B) {
  // function body
  return toNumber(A) + toNumber(B);
  
}
// function invocation
expect(plus).to.exist;
expect(plus("zero", "zero")).to.equal(0);
expect(plus("zero", "one")).to.equal(1);
```

## typeof
*The `typeof` operator returns a string indicating the type of the evaluated operand.*
- the `typeof` operator is followed by its operand.
- **Syntax:**
 - `typeof` *operand*

- **Parameters:**
 - *operand* is an expression representing the object or *primitive* whose type is to be returned.

- **Description:**
 - A summary of possible return values of `typeof`: 

Type | Result
---- | ------
Undefined | "undefined
Null | "object"
Boolean | "boolean"
Number | "number"
String | "string"
Symbol | "symbol"
Host object | *Implementation-dependant*
Function object | "function"
Any other object | "object"

- **Examples:**
```
// Numbers
typeof 37 === 'number';
typeof 3.14 === 'number';
typeof Math.LN2 === 'number';
typeof Infinity === 'number';
typeof NaN === 'number'; // Despite being "Not-A-Number"
typeof Number(1) === 'number'; // but never use this form!

// Strings
typeof "" === 'string';
typeof "bla" === 'string';
typeof (typeof 1) === 'string'; // typeof always return a string
typeof String("abc") === 'string'; // but never use this form!


// Booleans
typeof true === 'boolean';
typeof false === 'boolean';
typeof Boolean(true) === 'boolean'; // but never use this form!


// Symbols
typeof Symbol() === 'symbol'
typeof Symbol('foo') === 'symbol'
typeof Symbol.iterator === 'symbol'


// Undefined
typeof undefined === 'undefined';
typeof blabla === 'undefined'; // an undefined variable


// Objects
typeof {a:1} === 'object';


// use Array.isArray or Object.prototype.toString.call
// to differentiate regular objects from arrays
typeof [1, 2, 4] === 'object';

typeof new Date() === 'object';


// The following is confusing. Don't use!
typeof new Boolean(true) === 'object'; 
typeof new Number(1) === 'object'; 
typeof new String("abc") === 'object';


// Functions
typeof function(){} === 'function';
typeof class C {} === 'function';
typeof Math.sin === 'function';
```

## Array
- The JavaScript Array global object is a constructor for arrays, which are high-level, list-like objects.
### Syntax
```
[element0, element1, ..., elementN]
new Array(element0, element1[, ...[, elementN]])
new Array(arrayLength)
```
#### element*N*
 - A JavaScript array is initialized with the given elements, except in the case where a single argument is passed to the Array constructor and that argument is a number. (See below.) 
 - Note that this special case only applies to JavaScript arrays created with the Array constructor, not array literals created with the bracket syntax.
#### arrayLength
 - If the only argument passed to the Array constructor is an integer between 0 and 232-1 (inclusive), this returns a new JavaScript array with length set to that number. 
 - If the argument is any other number, a RangeError exception is thrown.
##### Array.prototype.length
 - The length property represents an unsigned, 32-bit integer that specifies the number of elements in an array.
 - **Syntax** 
  - `arr.length`
 - **Description**
  - The value of the length property is an integer with a positive sign and a value less than 2 to the 32nd power (232).
  - You can set the length property to truncate an array at any time. When you extend an array by changing its length property, the number of actual elements does not increase; for example, if you set length to 3 when it is currently 2, the array still contains only 2 elements. 
  - Thus, the length property says nothing about the number of defined values in the array. 
  - See also [Relationship between length and numerical properties](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#Relationship_between_length_and_numerical_properties).
- **Examples**
 - Example: *Iterating over an array*

In the following example the array numbers is iterated through by looking at the length property to see how many elements it has. The value in each element is then doubled.
```
var numbers = [1, 2, 3, 4, 5];

for (var i = 0; i < numbers.length; i++) {
  numbers[i] *= 2;
}
// numbers is now [2, 4, 6, 8, 10]
```
Example: *Shortening an array*

The following example shortens the array statesUS to a length of 50 if the current length is greater than 50.
```
if (statesUS.length > 50) {
  statesUS.length = 50;
}
```

### Array Literals
- An array literal is a list of zero or more expressions, each of which represents an array element, enclosed in square brackets ([ ]). 
- When you create an array using an array literal, it is initialized with the specified values as its elements, and its length is set to the number of arguments specified. 
- Examples:
```
var coffees = ["French Roast", "Colombian", "Kona"];
```
**Note:** An array literal is a type of object initializer. See Using [*Object Initializers*](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects#Using_object_initializers).
- Array literals are also Array objects.
##### Extra commas in array literals
  - You do not have to specify all elements in an array literal. 
  - If you put two commas in a row, the array is created with undefined for the unspecified elements. 
  - The following example creates the fish array:

  - `var fish = ["Lion", , "Angel"];`
This array has two elements with values and one empty element (fish[0] is "Lion", fish[1] is undefined, and fish[2] is "Angel").

  - If you include a trailing comma at the end of the list of elements, the comma is ignored. In the following example, the length of the array is three. There is no myList[3]. 
  - All other commas in the list indicate a new element. 
  - (Note: trailing commas can create errors in older browser versions and it is a best practice to remove them.)

`var myList = ['home', , 'school', ];`
  - In the following example, the length of the array is four, and myList[0] and myList[2] are missing.

`var myList = [ , 'home', , 'school'];`
  - In the following example, the length of the array is four, and myList[1] and myList[3] are missing. Only the last comma is ignored.

`var myList = ['home', , 'school', , ];`
  - Understanding the behavior of extra commas is important to understanding JavaScript as a language, however when writing your own code: explicitly declaring the missing elements as undefined will increase your code's clarity and maintainability.

### Non-Experimental Array Methods
##### Mutator Methods
They modify the array:

- **Array.prototype.pop()**
  - Removes the last element from an array and returns that element.
  - _params:_ none 
  - _returns:_ the last element 
  - _side-effects_: removes the element returned 
##### Example: Removing the last element of an array
```
var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];

console.log(myFish); // ['angel', 'clown', 'mandarin', 'sturgeon']

var popped = myFish.pop();

console.log(myFish); // ['angel', 'clown', 'mandarin' ] 

console.log(popped); // 'sturgeon'
```
- **Array.prototype.push()**
  - Adds one or more elements to the end of an array and returns the new length of the array.
  - _params:_ `element*N*` 
  - _returns:_ the new *length* property of the object upon which the method was called. 
  - _side-effects_: appends values to an array. 
##### Example: Adding elements to an array
- The following code creates the sports array containing two elements, then appends two elements to it. The total variable contains the new length of the array.
```
var sports = ['soccer', 'baseball'];
var total = sports.push('football', 'swimming');

console.log(sports); // ['soccer', 'baseball', 'football', 'swimming']
console.log(total);  // 4
```
##### Example: Merging two arrays
- This example uses apply() to push all elements from a second array.
```
var vegetables = ['parsnip', 'potato'];
var moreVegs = ['celery', 'beetroot'];

// Merge the second array into the first one
// Equivalent to vegetables.push('celery', 'beetroot');
Array.prototype.push.apply(vegetables, moreVegs);

console.log(vegetables); // ['parsnip', 'potato', 'celery', 'beetroot']
```
- **Array.prototype.reverse()**
  - Reverses the order of the elements of an array in place — the first becomes the last, and the last becomes the first.
- **Array.prototype.shift()**
  - Removes the first element from an array and returns that element.
- **Array.prototype.sort()**
  - Sorts the elements of an array in place and returns the array.
- **Array.prototype.splice()**
  - Adds and/or removes elements from an array.
- **Array.prototype.unshift()**
  - Adds one or more elements to the front of an array and returns the new length of the array.
##### Accessor methods
They **do not* modify the array and return some representation of the array.

- **Array.prototype.concat()**
  - Returns a new array comprised of this array joined with other array(s) and/or value(s).
- **Array.prototype.join()**
  - Joins all elements of an array into a string.
- **Array.prototype.slice()**
  - Extracts a section of an array and returns a new array.
- **Array.prototype.toString()**
  - Returns a string representing the array and its elements. Overrides the Object.prototype.toString() method.
- **Array.prototype.toLocaleString()**
  - Returns a localized string representing the array and its elements. Overrides the Object.prototype.toLocaleString() method.
- **Array.prototype.indexOf()**
  - Returns the first (least) index of an element within the array equal to the specified value, or -1 if none is found.
- **Array.prototype.lastIndexOf()**
  - Returns the last (greatest) index of an element within the array equal to the specified value, or -1 if none is found.







