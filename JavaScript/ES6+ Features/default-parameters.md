# 🧩 Default Parameters in JavaScript

---

## ✅ What Are Default Parameters?

**Default parameters** allow you to assign default values to function parameters **if no value is provided** or if the value is `undefined`.

> Introduced in **ES6** to avoid manual checks like `if (!param) {}`

---

## 🔧 Syntax

```js
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet("Vishnu"); // Hello, Vishnu!
greet();         // Hello, Guest!


function say(msg = "Hi") {
  console.log(msg);
}

say(undefined); // "Hi"
say(null);      // null
```