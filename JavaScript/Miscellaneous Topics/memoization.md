# 🧠 Memoization in JavaScript

---

## ✅ What is Memoization?

**Memoization** is a technique used to **cache the results** of expensive function calls so that if the same inputs occur again, the result can be returned from cache **instantly**, instead of re-computing.

---

## 🚀 Why Use It?

- Improves performance (especially for recursive or repeated computations)
- Reduces time complexity
- Saves resources

---

## 📦 Real-Life Example

Imagine you're computing the 40th Fibonacci number over and over. Without memoization, each call re-computes everything.

---

## 🧪 Basic Example

```js
function add(a, b) {
  console.log("Calculating...");
  return a + b;
}

function memoize(fn) {
  const cache = {};
  return function (...args) {
    const key = JSON.stringify(args);
    if (cache[key]) {
      return cache[key];
    } else {
      const result = fn(...args);
      cache[key] = result;
      return result;
    }
  };
}

const memoizedAdd = memoize(add);

console.log(memoizedAdd(2, 3)); // Calculating... 5
console.log(memoizedAdd(2, 3)); // From cache: 5
