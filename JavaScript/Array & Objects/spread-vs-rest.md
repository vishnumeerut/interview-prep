# 🌟 JavaScript Spread vs Rest Operators

The `...` (three dots) syntax in JavaScript can be used in two ways:
- 🔁 Spread Operator – to **expand** arrays or objects
- 🧺 Rest Operator – to **collect** multiple elements into a single variable

---

## 🔁 Spread Operator

> 📌 Use case: Expanding arrays or objects

### ✅ Spread with Arrays

```js
const arr1 = [1, 2];
const arr2 = [3, 4];
const combined = [...arr1, ...arr2];

console.log(combined); // [1, 2, 3, 4]
```


## 🧺 Rest Operator

> 📌 Use case: Collect remaining values into an array

### ✅ Rest in Function Parameters

```js
function sum(...numbers) {
  return numbers.reduce((acc, val) => acc + val, 0);
}
console.log(sum(1, 2, 3, 4)); // 10

```