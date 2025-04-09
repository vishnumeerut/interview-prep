# Explain Hoisting in javaScript


## 🧠 Definition:


- `Hoisting` :->  Hoisting is a phenomina where all the variables and functions can be execute before they initialize.
- 💡 Only declarations are hoisted, initializations are not.

- `Scope` :-> Scope refers to the current context in which variables, functions and objects are accessible within a program...

## 💻 Example Code:


```js

// ========================================
// Hoisting in JavaScript – Full Explanation
// ========================================

// --------------------
// ✅ Variable Hoisting with var
// --------------------


console.log(a); // Output: undefined
var a = 10;


// JavaScript hoists the declaration: var a;
// But the initialization (a = 10) stays in place.
// So console.log(a) prints undefined, not an error.


// --------------------
// ❌ Variable Hoisting with let
// --------------------

try {
  console.log(b); // ReferenceError
  let b = 20;
} catch (error) {
  console.error("let hoisting error:", error.message);
}

// let and const are hoisted but kept in a Temporal Dead Zone (TDZ).
// Accessing them before their declaration throws a ReferenceError.


// --------------------
// ❌ Variable Hoisting with const
// --------------------

try {
  console.log(c); // ReferenceError
  const c = 30;
} catch (error) {
  console.error("const hoisting error:", error.message);
}


// --------------------
// ✅ Function Hoisting (Function Declaration)
// --------------------

greet(); // Output: Hello!

function greet() {
  console.log("Hello!");
}

// Function declarations are fully hoisted,
// so we can call greet() before its definition.


// --------------------
// ❌ Function Expression is Not Hoisted
// --------------------

try {
  sayHi(); // TypeError: sayHi is not a function
  var sayHi = function () {
    console.log("Hi!");
  };
} catch (error) {
  console.error("Function expression hoisting error:", error.message);
}

// Only the variable 'sayHi' is hoisted (as undefined), not the function assigned to it.
// So calling sayHi() before the assignment throws a TypeError.

```
