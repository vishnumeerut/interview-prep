# 🔁 Generators in JavaScript

---

## ✅ What Are Generators?

Generators are special functions in JavaScript that can **pause** and **resume** their execution.  
They use the `function*` syntax and `yield` keyword to return values one by one.

---

## 🔧 Syntax

```js
function* generatorFunction() {
  yield 1;
  yield 2;
  yield 3;
}

// A generator returns an iterator object. You can call .next() on it to get values.

const gen = generatorFunction();

console.log(gen.next()); // { value: 1, done: false }
console.log(gen.next()); // { value: 2, done: false }
console.log(gen.next()); // { value: 3, done: false }
console.log(gen.next()); // { value: undefined, done: true }
