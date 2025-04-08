# 🔐 What is a Promise in JavaScript?

---

## ✅ Definition

A **Promise** is an object in JavaScript that represents the **eventual completion or failure** of an **asynchronous** operation.

It provides a cleaner way to write async code and replaces the need for deeply nested callbacks ("callback hell") and resolve the problem ("inversion of control").

---

## 🔁 States of a Promise

| State       | Description                               |
|-------------|-------------------------------------------|
| `pending`   | Initial state,     |
| `fulfilled` | Operation completed successfully          |
| `rejected`  | Operation failed                          |

---

## 🔧 Creating a Promise

```js
const promise = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("🎉 Task completed successfully");
  } else {
    reject("❌ Task failed");
  }
});

promise
  .then((result) => {
    console.log("Result:", result);
  })
  .catch((error) => {
    console.error("Error:", error);
  })
  .finally(() => {
    console.log("Promise completed...");
  });
