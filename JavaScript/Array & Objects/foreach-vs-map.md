# 🔁 Difference Between `forEach()` and `map()` in JavaScript

Both `forEach()` and `map()` are used to loop through arrays, but they serve different purposes.

---

## ✅ Quick Comparison

| Feature            | `forEach()`                      | `map()`                               |
|--------------------|----------------------------------|----------------------------------------|
| Purpose            | Executes a function on each item | Transforms each item and returns a new array |
| Return Value       | `undefined`                      | A new array                            |
| Chainable          | ❌ No                            | ✅ Yes                                  |
| Modifies Original? | ❌ No                            | ❌ No                                   |
| Use Case           | Side effects (logging, DOM ops)  | Data transformation                    |

---

## 🧪 Code Examples

### `forEach()`

```js
const numbers = [1, 2, 3];
numbers.forEach(num => {
  console.log(num * 2);
});

const result = numbers.forEach(num => num * 2);
console.log(result); // undefined
```

### `map()`

```js
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2);

console.log(doubled); // [2, 4, 6]

```
