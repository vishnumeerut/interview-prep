# What kind of API function is supported by Node.js?

Node.js supports **two main types** of API functions:

---

## ✅ 1. Asynchronous, Non-blocking APIs

- Do not wait for the result.
- Use callbacks, Promises, or async/await.
- Ideal for I/O operations like file reading, DB calls, or HTTP requests.

### 📦 Example:
```js
const fs = require("fs");
fs.readFile("file.txt", "utf8", (err, data) => {
  if (err) throw err;
  console.log(data);
});
```

---

## ⚠️ 2. Synchronous, Blocking APIs

- Wait for the task to finish before moving on.
- Can block the event loop — not ideal in production.

### 📦 Example:
```js
const fs = require("fs");
const data = fs.readFileSync("file.txt", "utf8");
console.log(data);
```

---

## 📌 Which One to Use?

- For most real-world apps, **asynchronous APIs are preferred** to keep Node.js non-blocking and performant.
- Synchronous APIs may be used during initialization or simple scripting.

