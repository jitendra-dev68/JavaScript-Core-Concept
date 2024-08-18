# Core JavaScript Concepts

## 1. **Basic Syntax and Operators**
- **Variables:**
  - `var`: Function-scoped variable. Can be redeclared and updated.
  - `let`: Block-scoped variable. Can be updated but not redeclared within the same block.
  - `const`: Block-scoped constant. Cannot be updated or redeclared. 

- **Data Types:**
  - **Primitive Types:** 
    - `string`: Represents text (e.g., `"hello"`).
    - `number`: Represents numeric values (e.g., `42`).
    - `boolean`: Represents `true` or `false`.
    - `null`: Represents intentional absence of any value.
    - `undefined`: Represents variables that have been declared but not assigned a value.
    - `symbol`: Represents a unique identifier (used mainly for object property keys).
    - `bigint`: Represents large integers beyond the range of the `number` type.

  - **Non-Primitive Types:**
    - `object`: Collections of key-value pairs (e.g., `{ name: "John" }`).
    - `array`: Ordered collections of values (e.g., `[1, 2, 3]`).

- **Operators:**
  - **Arithmetic:** 
    - `+`, `-`, `*`, `/`, `%` (addition, subtraction, multiplication, division, and modulus).
  - **Comparison:**
    - `==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=` (equality and relational comparisons).
  - **Logical:**
    - `&&` (logical AND), `||` (logical OR), `!` (logical NOT).

## 2. **Control Flow**
- **Conditionals:**
  - **`if`, `else if`, `else`:** Execute code based on boolean conditions.
  - **`switch`:** Select one of many code blocks to be executed based on a variable’s value.

- **Loops:**
  - **`for`:** Executes a block of code a number of times (e.g., `for (let i = 0; i < 5; i++) { console.log(i); }`).
  - **`while`:** Repeats a block of code as long as a condition is true (e.g., `while (i < 5) { console.log(i); i++; }`).
  - **`do...while`:** Executes a block of code once, and then repeats as long as a condition is true (e.g., `do { console.log(i); i++; } while (i < 5);`).

  - **Array Methods:**
    - `forEach`: Executes a function on each element of an array.
    - `map`: Creates a new array with the results of applying a function to each element.
    - `filter`: Creates a new array with elements that pass a test function.
    - `reduce`: Applies a function to reduce an array to a single value.

## 3. **Functions**
- **Function Declarations:**
  - Declared with the `function` keyword (e.g., `function add(a, b) { return a + b; }`).

- **Arrow Functions:**
  - Shorter syntax for function expressions (e.g., `(a, b) => a + b`).
  - Lexical `this` binding, which means `this` inside an arrow function is the same as `this` outside of it.

- **Function Scope:**
  - **Global Scope:** Accessible everywhere in the code.
  - **Local Scope:** Variables declared within a function are accessible only within that function.
  - **Closures:** Functions that retain access to their lexical scope even when the function is executed outside its scope.

- **Higher-Order Functions:**
  - Functions that either accept other functions as arguments or return functions (e.g., `Array.prototype.map`).

## 4. **Objects and Arrays**
- **Objects:**
  - Collections of key-value pairs (e.g., `{ name: "Alice", age: 30 }`).
  - **Methods:** Functions associated with objects (e.g., `person.greet = function() { return "Hello"; }`).

- **Arrays:**
  - Ordered collections of values (e.g., `[1, 2, 3, 4]`).
  - **Methods:** Operations on arrays such as `push`, `pop`, `shift`, `unshift`, `splice`, etc.
  - **Iteration:** `forEach`, `map`, `filter`, `reduce`.

## 5. **Asynchronous JavaScript**
- **Callbacks:**
  - Functions passed as arguments to other functions, executed after the completion of asynchronous operations.

- **Promises:**
  - Objects representing the eventual completion or failure of an asynchronous operation.
  - **States:** `pending`, `fulfilled`, `rejected`.
  - **Methods:** `then`, `catch`, `finally`.

- **Async/Await:**
  - **`async`:** Declares an asynchronous function that returns a promise.
  - **`await`:** Pauses the execution of an `async` function until the promise is resolved.

## 6. **Error Handling**
- **Try/Catch:**
  - **`try`:** Executes code that may throw an error.
  - **`catch`:** Handles errors thrown by the `try` block.
  - **`finally`:** Executes code after `try` and `catch` blocks, regardless of outcome.

- **Custom Errors:**
  - Create custom error types by extending the built-in `Error` class (e.g., `class CustomError extends Error { constructor(message) { super(message); this.name = "CustomError"; } }`).

## 7. **JavaScript Objects**
- **Prototype Inheritance:**
  - JavaScript objects inherit properties and methods from their prototypes.

- **Classes:**
  - **Syntax:** `class Person { constructor(name) { this.name = name; } greet() { return "Hello"; } }`.
  - Supports inheritance with `extends`.

- **Object Destructuring:**
  - Extract values from objects into variables (e.g., `const { name, age } = person;`).

- **Object Spread and Rest:**
  - **Spread:** Copy properties from one object to another (e.g., `{ ...obj1, ...obj2 }`).
  - **Rest:** Collect remaining properties into a new object (e.g., `const { a, ...rest } = obj;`).

## 8. **DOM Manipulation**
- **Selecting Elements:**
  - `getElementById`, `querySelector`, `querySelectorAll` for accessing DOM elements.

- **Manipulating Elements:**
  - **Text Content:** `element.textContent = "New text";`.
  - **Attributes:** `element.setAttribute("id", "newId");`.
  - **Styles:** `element.style.color = "blue";`.

- **Event Handling:**
  - **Adding Listeners:** `element.addEventListener("click", () => { console.log("Clicked!"); });`.
  - **Event Object:** Provides details about the event and methods for event handling.
  - **Propagation:** Event bubbling and capturing control how events propagate through the DOM.

## 9. **Modules**
- **ES6 Modules:**
  - **`import`:** Import functions, objects, or primitives from other modules (e.g., `import { myFunction } from './myModule.js';`).
  - **`export`:** Export functions, objects, or primitives from a module (e.g., `export const myFunction = () => { /* ... */ };`).

- **Module Bundlers:**
  - Tools like Webpack, Rollup, or Parcel bundle multiple modules into a single file or multiple optimized files.

## 10. **JavaScript Engine and Performance**
- **Execution Context:**
  - The environment in which JavaScript code is executed, including the global context and function contexts.

- **Garbage Collection:**
  - Automatic process of reclaiming memory by removing objects that are no longer needed.

- **Performance Optimization:**
  - Techniques such as minimizing DOM manipulations, avoiding memory leaks, and optimizing loops.

## 11. **Security Considerations**
- **Common Vulnerabilities:**
  - **XSS (Cross-Site Scripting):** Injecting malicious scripts into web pages.
  - **CSRF (Cross-Site Request Forgery):** Unauthorized commands transmitted from a user that the web application trusts.

- **Best Practices:**
  - Validate and sanitize input data, use secure coding practices, and regularly update dependencies.

## 12. **Browser APIs**
- **Fetch API:**
  - Modern interface for making network requests (e.g., `fetch(url).then(response => response.json()).then(data => console.log(data));`).

- **Local Storage and Session Storage:**
  - **Local Storage:** Persistent data storage (e.g., `localStorage.setItem("key", "value");`).
  - **Session Storage:** Temporary data storage for a session (e.g., `sessionStorage.setItem("key", "value");`).

- **Geolocation API:**
  - Access the user’s geographical location (e.g., `navigator.geolocation.getCurrentPosition(success, error);`).

## 13. **Advanced Topics**
- **Closures:**
  - Functions with access to variables from their lexical scope, even after the outer function has returned.

- **Currying and Partial Application:**
  - **Currying:** Transforming a function with multiple arguments into a
