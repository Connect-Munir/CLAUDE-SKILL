# JavaScript Basics Flashcards

## Deck: JavaScript Fundamentals
**Target Audience**: Beginners
**Total Cards**: 20
**Difficulty Progression**: Beginner → Intermediate

---

## 1. Variables & Data Types

### Card 1
**Question**: What are the three ways to declare variables in JavaScript?

**Answer**:
- `var` - Function-scoped, can be re-declared (older approach)
- `let` - Block-scoped, cannot be re-declared (modern, recommended)
- `const` - Block-scoped, cannot be re-declared or reassigned (for constants)

**Category**: Variables
**Difficulty**: Beginner
**Example**:
```javascript
var name = "John";      // var
let age = 30;           // let (preferred)
const country = "USA";  // const (for constants)
```

---

### Card 2
**Question**: What are the primitive data types in JavaScript?

**Answer**:
- `number` - Integers and decimals (42, 3.14)
- `string` - Text enclosed in quotes ("hello", 'world')
- `boolean` - True or false values
- `null` - Intentional absence of value
- `undefined` - Variable declared but not assigned
- `symbol` - Unique identifier (ES6+)
- `bigint` - Large integers beyond number limit (ES11+)

**Category**: Data Types
**Difficulty**: Beginner
**Example**:
```javascript
let num = 42;
let text = "Hello";
let flag = true;
let empty = null;
let notDefined = undefined;
```

---

### Card 3
**Question**: What is the difference between `null` and `undefined`?

**Answer**:
- `null` - An assignment value representing "no value" (intentional)
- `undefined` - Default value for uninitialized variables (unintentional)

**Category**: Data Types
**Difficulty**: Beginner
**Example**:
```javascript
let x = null;        // explicitly set to null
let y;               // undefined (not assigned)
let z = undefined;   // explicitly set to undefined
```

---

## 2. Operators & Expressions

### Card 4
**Question**: What is the difference between `==` and `===` in JavaScript?

**Answer**:
- `==` (loose equality) - Compares values after type coercion
- `===` (strict equality) - Compares both value and type without conversion

**Category**: Operators
**Difficulty**: Beginner
**Example**:
```javascript
5 == "5"   // true (loose: converts string to number)
5 === "5"  // false (strict: different types)
5 === 5    // true (strict: same value and type)
```

---

### Card 5
**Question**: What does the ternary operator do? Give the syntax.

**Answer**:
The ternary operator is a shorthand for if-else statements:
- **Syntax**: `condition ? valueIfTrue : valueIfFalse`
- Returns different values based on the condition

**Category**: Operators
**Difficulty**: Beginner
**Example**:
```javascript
let age = 20;
let status = age >= 18 ? "Adult" : "Minor";
console.log(status); // "Adult"
```

---

### Card 6
**Question**: What are truthy and falsy values in JavaScript?

**Answer**:
**Falsy values** (convert to false):
- `false`, `0`, `""` (empty string), `null`, `undefined`, `NaN`

**Truthy values** (convert to true):
- Everything else! Non-zero numbers, non-empty strings, objects, arrays, functions

**Category**: Operators
**Difficulty**: Beginner
**Example**:
```javascript
if ("hello") { }    // true - non-empty string is truthy
if ("") { }         // false - empty string is falsy
if (0) { }          // false - zero is falsy
if (1) { }          // true - non-zero number is truthy
```

---

## 3. Control Flow

### Card 7
**Question**: What is the difference between `for`, `while`, and `do...while` loops?

**Answer**:
- `for` - Loops a specific number of times with counter
- `while` - Loops as long as condition is true (checks before executing)
- `do...while` - Loops as long as condition is true (executes at least once)

**Category**: Control Flow
**Difficulty**: Beginner
**Example**:
```javascript
for (let i = 0; i < 3; i++) { }        // for loop
while (condition) { }                   // while loop
do { } while (condition);               // do-while loop
```

---

### Card 8
**Question**: What does the `switch` statement do? Give the syntax.

**Answer**:
The switch statement checks a value against multiple cases:
- Compares a value to multiple options
- Executes code for the matching case
- `break` prevents fall-through to next case
- `default` executes if no case matches

**Category**: Control Flow
**Difficulty**: Beginner
**Example**:
```javascript
let day = 3;
switch(day) {
  case 1: console.log("Monday"); break;
  case 2: console.log("Tuesday"); break;
  case 3: console.log("Wednesday"); break;
  default: console.log("Other day");
}
```

---

## 4. Functions

### Card 9
**Question**: What is the difference between function declaration and function expression?

**Answer**:
- **Function Declaration**: `function name() { }` - Hoisted (can be called before declaration)
- **Function Expression**: `const name = function() { }` - Not hoisted (must be declared before calling)
- **Arrow Function**: `const name = () => { }` - Modern, concise syntax (ES6+)

**Category**: Functions
**Difficulty**: Beginner
**Example**:
```javascript
greet();  // Works - function declaration is hoisted

function greet() { console.log("Hello"); }

// vs
sayBye();  // Error - not hoisted

const sayBye = function() { console.log("Bye"); };
```

---

### Card 10
**Question**: What is an arrow function? What are its advantages?

**Answer**:
Arrow function is a concise syntax for writing functions using `=>`

**Advantages**:
- Shorter, cleaner syntax
- Implicit return for single expressions
- `this` is inherited from parent scope (not bound to function)

**Category**: Functions
**Difficulty**: Intermediate
**Example**:
```javascript
// Regular function
function add(a, b) { return a + b; }

// Arrow function
const add = (a, b) => a + b;  // implicit return

// Multiple statements
const multiply = (a, b) => {
  const result = a * b;
  return result;
};
```

---

### Card 11
**Question**: What are function parameters and arguments? What is the difference?

**Answer**:
- **Parameters** - Variables defined in function declaration
- **Arguments** - Actual values passed when calling the function

**Category**: Functions
**Difficulty**: Beginner
**Example**:
```javascript
// name and age are PARAMETERS
function printInfo(name, age) {
  console.log(name, age);
}

// "John" and 30 are ARGUMENTS
printInfo("John", 30);
```

---

## 5. Objects & Arrays

### Card 12
**Question**: What is an object in JavaScript? How do you create one?

**Answer**:
An object is a collection of key-value pairs storing related data and functionality.

**Creation methods**:
- Object literal: `const obj = { key: value }`
- Constructor: `const obj = new Object()`
- Object.create(): `Object.create(prototype)`

**Category**: Objects
**Difficulty**: Beginner
**Example**:
```javascript
const person = {
  name: "John",
  age: 30,
  city: "New York",
  greet: function() { console.log("Hello"); }
};

console.log(person.name);     // "John"
console.log(person["age"]);   // 30
person.greet();               // "Hello"
```

---

### Card 13
**Question**: What is an array in JavaScript? How do you access elements?

**Answer**:
An array is an ordered collection of elements (can contain any data type).

**Accessing elements**:
- By index: `array[0]` (first element)
- Array indexing is 0-based (first element at index 0)
- Out of bounds returns `undefined`

**Category**: Arrays
**Difficulty**: Beginner
**Example**:
```javascript
const colors = ["red", "green", "blue"];
console.log(colors[0]);    // "red"
console.log(colors[2]);    // "blue"
console.log(colors.length); // 3
colors[1] = "yellow";      // modify element
```

---

### Card 14
**Question**: What are common array methods? Name at least 5.

**Answer**:
- `push()` - Add element to end
- `pop()` - Remove last element
- `shift()` - Remove first element
- `unshift()` - Add element to beginning
- `slice()` - Extract portion without modifying original
- `splice()` - Add/remove elements
- `map()` - Transform each element
- `filter()` - Keep elements matching condition
- `reduce()` - Combine into single value

**Category**: Arrays
**Difficulty**: Intermediate
**Example**:
```javascript
let arr = [1, 2, 3];
arr.push(4);           // [1, 2, 3, 4]
arr.pop();             // [1, 2, 3]
arr.map(x => x * 2);   // [2, 4, 6]
arr.filter(x => x > 1); // [2, 3]
```

---

## 6. String Methods

### Card 15
**Question**: What are common string methods? Name at least 5.

**Answer**:
- `length` - Get string length
- `toUpperCase()` - Convert to uppercase
- `toLowerCase()` - Convert to lowercase
- `slice()` - Extract portion of string
- `substring()` - Extract between indices
- `indexOf()` - Find position of text
- `includes()` - Check if contains text
- `split()` - Split into array
- `trim()` - Remove whitespace
- `replace()` - Replace text

**Category**: Strings
**Difficulty**: Beginner
**Example**:
```javascript
let text = "  Hello World  ";
text.toUpperCase();        // "  HELLO WORLD  "
text.toLowerCase();        // "  hello world  "
text.trim();               // "Hello World"
text.includes("World");    // true
text.split(" ");           // ["", "", "Hello", "World", "", ""]
text.slice(2, 7);          // "Hello"
```

---

## 7. Scope & Hoisting

### Card 16
**Question**: What is scope in JavaScript? What types of scope exist?

**Answer**:
Scope determines where variables are accessible.

**Types of scope**:
- **Global Scope** - Accessible everywhere
- **Function Scope** - Accessible only within function
- **Block Scope** - Accessible only within block (if, for, while) - `let` and `const`
- **Lexical Scope** - Inner functions can access outer function variables

**Category**: Scope & Hoisting
**Difficulty**: Intermediate
**Example**:
```javascript
let global = "global";      // global scope

function outer() {
  let outerVar = "outer";   // function scope

  if (true) {
    let blockVar = "block"; // block scope
  }

  console.log(outerVar);    // works
  console.log(blockVar);    // Error - not in scope
}
```

---

### Card 17
**Question**: What is hoisting in JavaScript?

**Answer**:
Hoisting is JavaScript's behavior of moving declarations to the top of scope before execution.

**What gets hoisted**:
- Function declarations - fully hoisted (can be called before declaration)
- `var` declarations - hoisted but not initialized (undefined)
- `let` and `const` - hoisted but not initialized (Temporal Dead Zone)

**Category**: Scope & Hoisting
**Difficulty**: Intermediate
**Example**:
```javascript
console.log(x);     // undefined (hoisted but not initialized)
var x = 5;

console.log(y);     // Error - let is hoisted but in "Temporal Dead Zone"
let y = 10;

greet();            // Works - function declaration fully hoisted
function greet() { console.log("Hi"); }
```

---

## 8. Closures & `this`

### Card 18
**Question**: What is a closure in JavaScript?

**Answer**:
A closure is a function that has access to variables from its outer (parent) function scope, even after the outer function has returned.

**Why use closures**:
- Data encapsulation/privacy
- Creating functions that "remember" values
- Factory functions and callbacks

**Category**: Closures
**Difficulty**: Intermediate
**Example**:
```javascript
function counter() {
  let count = 0;

  return function() {
    count++;
    return count;
  };
}

const increment = counter();
console.log(increment()); // 1
console.log(increment()); // 2
console.log(increment()); // 3
// count variable is "closed over" by the returned function
```

---

### Card 19
**Question**: What is `this` in JavaScript? What does it refer to?

**Answer**:
`this` refers to the object that is executing the current code.

**Value depends on context**:
- **Regular function** - `this` = global object (window in browser, global in Node.js)
- **Method** - `this` = the object the method belongs to
- **Arrow function** - `this` = inherited from parent scope
- **Constructor** - `this` = new object being created

**Category**: this Keyword
**Difficulty**: Intermediate
**Example**:
```javascript
const person = {
  name: "John",
  greet: function() {
    console.log(this.name);  // "John" - this = person object
  },
  arrowGreet: () => {
    console.log(this);       // window/global - inherited this
  }
};

person.greet();       // "John"
```

---

## 9. Async JavaScript

### Card 20
**Question**: What is the difference between synchronous and asynchronous code?

**Answer**:
- **Synchronous** - Code executes line by line; each line waits for previous to finish
- **Asynchronous** - Code can execute without waiting; useful for time-consuming operations (API calls, file reading)

**Methods for async**:
- Callbacks
- Promises
- Async/await

**Category**: Async
**Difficulty**: Intermediate
**Example**:
```javascript
// Synchronous
console.log("Start");
console.log("Middle");
console.log("End");
// Output: Start → Middle → End (in order)

// Asynchronous
console.log("Start");
setTimeout(() => console.log("Middle"), 1000);
console.log("End");
// Output: Start → End → Middle (after 1 second)
```

---

## Study Guide

**Recommended Study Order**:
1. Cards 1-3 (Variables & Data Types)
2. Cards 4-6 (Operators)
3. Cards 7-8 (Control Flow)
4. Cards 9-11 (Functions)
5. Cards 12-15 (Objects, Arrays, Strings)
6. Cards 16-17 (Scope & Hoisting)
7. Cards 18-19 (Closures & this)
8. Card 20 (Async Basics)

**Next Steps After Mastering Basics**:
- Promises and async/await
- ES6+ features (destructuring, spread operator, classes)
- DOM manipulation
- Event handling
- Error handling (try/catch)
- Regular expressions

