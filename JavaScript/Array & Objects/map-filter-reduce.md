# 🔁 JavaScript Array Methods: `map()`, `filter()`, and `reduce()`

These methods are powerful tools for transforming, filtering, and summarizing data in arrays.

---

## 1. `map()` – Transform Each Element

**Definition**: Returns a **new array** by applying a function to every element in the original array.

```js
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8]
```

## 2. `filter()` – Select Matching Elements

**Definition**: Returns a **new array** containing only the elements that pass a given test (truthy condition).


```js
const numbers = [1, 2, 3, 4, 5];
const even = numbers.filter(num => num % 2 === 0);
console.log(even); // [2, 4]

```

## 1. `reduce()` – Accumulate to a Single Value


**Definition**: Reduces the array to a **single value** by executing a callback on each element.


```js
const numbers = [1, 2, 3, 4];
const total = numbers.reduce((acc, curr) => acc + curr, 0);
console.log(total); // 10

```