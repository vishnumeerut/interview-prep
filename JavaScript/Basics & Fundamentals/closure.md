### 🔒 What is a Closure in JavaScript?

A **closure** is the combination of  function bundle together with reference to it's lexical enviornment.

It **remembers its outer scope**, even after the outer function has finished executing.

Closures allow you to **access variables** from an **outer function scope** even after the outer function has returned.

- 💡 Closure's value is stored inside Heap Memory...


---

### 📦 Example:

```js
function outerFunction() {
  let count = 0;

  function innerFunction() {
    count++;
    console.log("Count:", count);
  }

  return innerFunction;
}

const counter = outerFunction();
counter(); // Count: 1
counter(); // Count: 2
