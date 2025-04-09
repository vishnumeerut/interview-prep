# ❌ Types of Errors in JavaScript

---

## 🧩 1. SyntaxError

Occurs when the code has **invalid syntax** that prevents the JS engine from parsing it.

```js
// ❌ Missing closing parenthesis
if (true {
  console.log("Oops!");
}
```

## 🧩 2. ReferenceError

Happens when trying to **access a variable** that doesn't exist.
```js
console.log(x); // ❌ ReferenceError: x is not defined

```

## 🧩 3. TypeError

Occurs when a **value is not of the expected type** (e.g., calling something that isn't a function).

```js
const num = 5;
num(); // ❌ TypeError: num is not a function

```


## 🧩 4. RangeError

Thrown when a value is **out of an acceptable range**.
```js

// ❌ Too many digits in toFixed
let num = 1;
num.toFixed(1000); // RangeError


```