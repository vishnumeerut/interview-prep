# 🛠️ try...catch in JavaScript

---

## 🔍 What Is `try...catch`?

`try...catch` is used to **handle errors gracefully** in JavaScript.  
It allows you to run code that may throw an error, and catch it without crashing the program.

---

## 🧱 Syntax

```js
try {
  // Code that may throw an error
} catch (error) {
  // Handle the error here
}


try {
  let result = 10 / 0;
  console.log(result);
  unknownFunction(); // ❌ This will throw a ReferenceError
} 
catch (err) {
  console.error("Something went wrong:");
  console.error(err.name);    // e.g., ReferenceError
  console.error(err.message); // e.g., unknownFunction is not defined
}
