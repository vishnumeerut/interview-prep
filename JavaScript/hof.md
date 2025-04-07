## 🔹 What are Higher-Order Functions in JavaScript?

- A **Higher-Order Function** is a function that takes another function as an argument,      or returns a function from functions.

- In JavaScript, functions are **first-class citizens**, meaning they can be assigned to variables, passed as arguments, and returned from other functions.

- Common examples of higher-order functions: `map()`, `filter()`, `reduce()`, `forEach()`.

### ✅ Example:
```js
function greet(name) {
  return `Hello, ${name}`;
}

function processUser(name, callback) {
  return callback(name);
}

console.log(processUser("Vishnu", greet)); // Output: Hello, Vishnu
