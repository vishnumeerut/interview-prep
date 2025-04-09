# ⚡ IIFE (Immediately Invoked Function Expression)

## ✅ What is an IIFE?

An **IIFE (Immediately Invoked Function Expression)** is a function in JavaScript that is **executed as soon as it is defined**.

The main purpose of an IIFE is to **create a private scope** and avoid polluting the **global namespace**.

---

## 🔧 Syntax

```js
(function () {
  let name = "Vishnu";
  console.log("Hello " + name); // Hello Vishnu
})();


// name is not accessible outside
console.log(name); // ❌ ReferenceError

