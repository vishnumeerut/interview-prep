# 🧰 Most Useful Console Methods in JavaScript

JavaScript’s `console` object provides several methods that are incredibly useful for debugging and inspecting data during development.

---

## ✅ 1. `console.log()`

Used to log general-purpose messages, variables, or output.

```js
console.log("Hello Vishnu!");
```

## ⚠️ 2. `console.warn()`

Displays a warning message in yellow in the console.

```js
console.warn("This is just a warning.");
```


## ❌ 3. `console.error()`

Displays an error message in red, useful for debugging errors.

```js
console.error("Something went wrong!");
```


## 📊 4. `console.table()`

Displays data (like arrays or objects) in a tabular format.
```js
const users = [
  { id: 1, name: "Vishnu" },
  { id: 2, name: "Kumar" },
];

console.table(users);


```
## ⏱️ 5. `console.time()` and `console.timeEnd()`

Used to measure how long a block of code takes to execute.

```js
console.time("Timer");
for (let i = 0; i < 100000; i++) {}
console.timeEnd("Timer"); // Output: Timer: 2.5ms

```