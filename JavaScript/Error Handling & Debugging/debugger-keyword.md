# 🐞 `debugger` Keyword in JavaScript

---

## 🧠 What Is `debugger`?

The `debugger` statement **pauses the execution of JavaScript** and lets you inspect variables, the call stack, and scope at that specific point using browser developer tools.

It's like setting a **manual breakpoint** in your code.

---

## 📘 Syntax

```js
debugger;
function calculateSum(a, b) {
  let result = a + b;
  debugger; // Code pauses here if DevTools are open
  return result;
}

calculateSum(5, 3);
```
### When the browser encounters debugger, it pauses code execution if DevTools are open.