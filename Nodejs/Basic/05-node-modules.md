# What is a module in Node.js?

A **module** in Node.js is a reusable block of code that can be used across different files.

Node.js follows the **CommonJS** module system, where each file is treated as a module.

---

## 📂 Types of Modules

1. **Built-in Modules** – Provided by Node.js (e.g., `fs`, `path`, `http`).
2. **User-defined Modules** – Custom files created by developers.
3. **Third-party Modules** – Installed using npm (e.g., `express`, `lodash`).

---

## 🧪 Example: Creating a Custom Module

### math.js
```js
function add(a, b) {
  return a + b;
}
module.exports = add;
```

### app.js
```js
const add = require('./math');
console.log(add(2, 3)); // Output: 5
```

---

## 🚀 Benefits of Using Modules

- Improves **code organization**
- Encourages **code reuse**
- Enables **separation of concerns**

