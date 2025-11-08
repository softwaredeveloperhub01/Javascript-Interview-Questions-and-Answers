# Javascript Interview Questions and Answers

> Javascript Interviews – Top Questions &amp; Answers for Web Developers

---

## Core JavaScript Basics

### 1. What is JavaScript?
JavaScript is a lightweight, interpreted programming language used to build dynamic web pages. It runs in browsers and on servers (via Node.js).

---

### 2. What are primitive data types in JavaScript?
`string`, `number`, `boolean`, `null`, `undefined`, `symbol`, and `bigint`.

*Remember:* “SNB-NUBS” – String, Number, Boolean, Null, Undefined, BigInt, Symbol.

---

### 3. Difference between `null` and `undefined`?
- `undefined`: a variable declared but not assigned.
- `null`: an intentional empty value.

```js
let a; // undefined
let b = null; // null
````

---

### 4. What is `typeof null`?

It returns `"object"` — a long-standing bug in JavaScript.

---

### 5. How does `==` differ from `===`?

* `==` checks value equality after type coercion.
* `===` checks value and type equality (strict).

---

### 6. What is NaN?

NaN means “Not-a-Number”, but it’s actually of type `number`.

```js
typeof NaN; // "number"
```

---

### 7. How to check if a value is NaN?

Use `Number.isNaN(value)` instead of `isNaN()` for accuracy.

---

### 8. What is hoisting?

Variables and functions are moved to the top of their scope before execution.

```js
console.log(x); // undefined
var x = 5;
```

---

### 9. Difference between `var`, `let`, and `const`?

* `var`: function-scoped, hoisted.
* `let`: block-scoped, re-assignable.
* `const`: block-scoped, not re-assignable.

---

### 10. What are template literals?

String literals enclosed by backticks `` ` `` that support interpolation.

```js
const name = "Parth";
console.log(`Hello, ${name}!`);
```

---

## Functions & Scope

### 11. What is a function expression?

A function assigned to a variable.

```js
const greet = function() { return "Hi"; };
```

---

### 12. What is an arrow function?

A shorter syntax for writing functions, without its own `this`.

```js
const add = (a, b) => a + b;
```

---

### 13. Difference between function declaration and expression?

* Declarations are hoisted.
* Expressions are not.

---

### 14. What is closure?

A closure is when an inner function remembers variables from its outer scope even after the outer function has finished.

```js
function counter() {
  let count = 0;
  return () => ++count;
}
```

---

### 15. What is a callback function?

A function passed as an argument to another function to execute later.

---

### 16. What is the difference between synchronous and asynchronous code?

* **Synchronous:** blocks until finished.
* **Asynchronous:** doesn’t block, uses callbacks, promises, or async/await.

---

### 17. What is the event loop?

It’s the mechanism that handles asynchronous code execution in JavaScript.

---

### 18. What is lexical scope?

Scope determined by the physical placement of code — nested functions can access outer variables.

---

### 19. What is IIFE?

Immediately Invoked Function Expression — runs immediately after creation.

```js
(function() {
  console.log("Run instantly");
})();
```

---

### 20. What is recursion?

A function calling itself until a condition is met.

---

## Arrays & Objects

### 21. What are array methods in JS?

* Mutating: `push`, `pop`, `splice`
* Non-mutating: `map`, `filter`, `reduce`, `concat`

---

### 22. Difference between `forEach` and `map`?

* `forEach`: executes a function for each element (no return).
* `map`: returns a new array.

---

### 23. How to clone an array?

```js
const copy = [...arr];
```

---

### 24. How to merge arrays?

```js
const all = [...arr1, ...arr2];
```

---

### 25. How to remove duplicates from an array?

```js
const unique = [...new Set(arr)];
```

---

### 26. Difference between shallow and deep copy?

* **Shallow:** copies only one level.
* **Deep:** copies nested objects too.

---

### 27. What is destructuring?

Extracting values from arrays/objects easily.

```js
const [x, y] = [1, 2];
const {name, age} = user;
```

---

### 28. How to merge two objects?

```js
const merged = {...obj1, ...obj2};
```

---

### 29. How to check if object is empty?

```js
Object.keys(obj).length === 0
```

---

### 30. What is optional chaining?

Safely accessing nested properties.

```js
user?.profile?.email;
```

---

## ES6+ Concepts

### 31. What is destructuring assignment?

Allows unpacking values from arrays or properties from objects.

---

### 32. What are default parameters?

Default values for function parameters.

```js
function greet(name = "Guest") {}
```

---

### 33. What are rest parameters?

Collects all arguments into an array.

```js
function sum(...nums) {}
```

---

### 34. What is the spread operator?

Expands an iterable into elements.

```js
[...arr1, ...arr2];
```

---

### 35. What are modules in JS?

Reusable code blocks using `export` and `import`.

---

### 36. What are generators?

Functions that can pause and resume with `yield`.

---

### 37. What is a symbol?

A unique and immutable identifier.

---

### 38. What is BigInt?

A data type for very large integers.

```js
const big = 123456789012345678901234567890n;
```

---

### 39. What are tagged templates?

Custom string processing with functions.

---

### 40. What is `Proxy` in JS?

An object that intercepts operations like get/set.

---

## Asynchronous JS

### 41. What is a Promise?

An object that represents the eventual completion (or failure) of an async operation.

---

### 42. What are promise states?

Pending → Fulfilled → Rejected.

---

### 43. What is async/await?

Syntactic sugar for promises that makes async code look synchronous.

---

### 44. What is `Promise.all`?

Waits for all promises to resolve.

---

### 45. Difference between `Promise.all` and `Promise.race`?

* `all`: waits for all.
* `race`: returns first settled one.

---

### 46. What is event bubbling?

Events propagate from child to parent.

---

### 47. What is event capturing?

Events propagate from parent to child.

---

### 48. How to stop event propagation?

```js
event.stopPropagation();
```

---

### 49. What is `this` in JavaScript?

`this` refers to the context in which a function is executed.

---

### 50. What is call, apply, and bind?

* `call` – calls with arguments.
* `apply` – calls with array.
* `bind` – returns a new function.

---

## Advanced Topics

### 51. What is prototype in JS?

Each object has a hidden `[[Prototype]]` that forms the prototype chain.

---

### 52. What is prototypal inheritance?

Objects inherit properties from other objects via prototypes.

---

### 53. Difference between classical and prototypal inheritance?

Classical uses classes; prototypal uses objects directly.

---

### 54. What is `Object.create()`?

Creates an object with a specific prototype.

---

### 55. What are higher-order functions?

Functions that take other functions as arguments or return them.

---

### 56. What is currying?

Breaking a function with multiple arguments into a series of single-argument functions.

---

### 57. What is memoization?

Caching the results of expensive function calls.

---

### 58. What is debouncing?

Delays execution of a function until after a pause.

---

### 59. What is throttling?

Ensures a function runs at most once in a time window.

---

### 60. What is event delegation?

Attaching one event listener to a parent instead of multiple children.

---

## Browser & DOM

### 61. What is DOM?

Document Object Model — tree representation of the HTML document.

---

### 62. How to select DOM elements?

`getElementById`, `querySelector`, `querySelectorAll`.

---

### 63. What is the difference between innerHTML and textContent?

* `innerHTML`: parses HTML.
* `textContent`: only text.

---

### 64. What are data attributes?

Custom attributes starting with `data-` for embedding custom data.

---

### 65. What is localStorage vs sessionStorage?

* `localStorage`: persistent.
* `sessionStorage`: cleared when tab closes.

---

### 66. What is cookie vs localStorage?

Cookies sent with requests; localStorage is client-side only.

---

### 67. What is Fetch API?

Modern interface to make HTTP requests.

---

### 68. How to handle JSON in JS?

`JSON.parse()` and `JSON.stringify()`.

---

### 69. What is CORS?

Cross-Origin Resource Sharing — controls access between different origins.

---

### 70. What is a service worker?

A background script that enables offline experiences and caching.

---

## Error Handling & Performance

### 71. How to handle errors in JS?

Use `try...catch`.

---

### 72. What is the difference between runtime and syntax errors?

Syntax errors prevent execution; runtime occurs during execution.

---

### 73. What is debugging?

Finding and fixing errors using tools like Chrome DevTools.

---

### 74. How to prevent memory leaks?

Remove event listeners, avoid global variables, and clear timers.

---

### 75. What is garbage collection?

Automatic memory cleanup by removing unused objects.

---

## Object-Oriented JS

### 76. What is a class in JS?

Blueprint for creating objects.

---

### 77. What are constructors?

Special functions for initializing objects.

---

### 78. What are class inheritance and `super()`?

Allows extending another class and accessing parent methods.

---

### 79. What are getters and setters?

Methods to get and set properties.

---

### 80. What is static method?

Belongs to the class, not the instance.

---

## Miscellaneous

### 81. What is the difference between shallow and deep comparison?

Shallow checks references; deep compares values recursively.

---

### 82. What is immutability?

Data that cannot be modified after creation.

---

### 83. What are pure functions?

Functions that return the same output for the same input and have no side effects.

---

### 84. What is JSON?

JavaScript Object Notation — lightweight format for data exchange.

---

### 85. What is a polyfill?

Code that implements modern features in older browsers.

---

### 86. What is transpiling?

Converting modern JS to older syntax (e.g., via Babel).

---

### 87. What is tree shaking?

Removing unused code during bundling.

---

### 88. What are modules and bundlers?

Modules are reusable code units; bundlers (Webpack, Vite) combine them.

---

### 89. What is event-driven programming?

Program flow controlled by events.

---

### 90. What is REPL?

Read-Eval-Print Loop — an interactive shell for JS.

---

## Modern JavaScript Concepts

### 91. What is optional chaining used for?

To safely access nested properties without errors.

---

### 92. What is the nullish coalescing operator?

Returns the right-hand operand when the left is `null` or `undefined`.

```js
value ?? "default";
```

---

### 93. What are WeakMap and WeakSet?

Collections that hold weak object references, not preventing garbage collection.

---

### 94. What is dynamic import?

Loads modules lazily.

```js
import('./module.js');
```

---

### 95. What is the difference between map and weakMap?

WeakMap keys must be objects and are not iterable.

---

### 96. What is microtask vs macrotask?

Microtasks: promises; Macrotasks: setTimeout, I/O.

---

### 97. What is shadow DOM?

Encapsulated DOM for web components.

---

### 98. What is a web worker?

Runs JavaScript in a background thread for parallel processing.

---

### 99. What is the difference between deep copy and structuredClone()?

`structuredClone()` creates a deep copy including nested objects safely.

---

### 100. Why is JavaScript single-threaded?

Because it uses a single main thread and event loop model — concurrency is handled via async mechanisms.

---