# ⏰ Difference Between `setTimeout()` and `setInterval()` in JavaScript

---

## 📘 Definition

| Function         | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| `setTimeout()`   | Executes a function **once after a delay** (in milliseconds)                |
| `setInterval()`  | Executes a function **repeatedly at regular intervals** (in milliseconds)   |

---

## 🧠 Syntax

```js
// setTimeout
setTimeout(callback, delay);

// setInterval
setInterval(callback, interval);

💻 Example: setTimeout

setTimeout(() => {
  console.log("Runs once after 2 seconds");
}, 2000);


💻 Example: setInterval

setInterval(() => {
  console.log("Runs every 2 seconds");
}, 2000);
