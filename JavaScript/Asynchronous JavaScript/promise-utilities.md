# 🔗 Promise.all(), Promise.allSettled(), Promise.race(), and Promise.any()

---

## ✅ Purpose

These methods are used to handle **multiple Promises** in parallel and respond based on how they resolve.

---

## 🔹 1. Promise.all()

- Waits for **all Promises to resolve**
- If **any** Promise rejects, return the value of **rejectd promise**

```js
const p1 = Promise.resolve(1);
const p2 = Promise.resolve(2);
const p3 = Promise.resolve(3);

Promise.all([p1, p2, p3])
  .then((values) => console.log("✅", values)) // [1, 2, 3]
  .catch((err) => console.error("❌", err));

```

## 🔹 2. Promise.allSettled()

- Waits for **all Promises to finish**
- Returns an **array of objects** with `all` fullfilled or rejected promises.

```js

const p1 = Promise.resolve("✅ Success");
const p2 = Promise.reject("❌ Failed");

Promise.allSettled([p1, p2]).then((results) => {
  console.log(results);

});
// [
//   { status: "fulfilled", value: "✅ Success" },
//   { status: "rejected", reason: "❌ Failed" }
// ]

```

## 🔹 3. Promise.race()

- Returns as soon as `any` Promise settles **(either resolves or rejects)**
- You get the `value` of the first settled Promise.

```js

const p1 = new Promise((res) => setTimeout(() => res("⚡ Fast"), 100));
const p2 = new Promise((res) => setTimeout(() => res("🐢 Slow"), 1000));

Promise.race([p1, p2]).then((value) => console.log(value)); // ⚡ Fast


```

## 🔹 4. Promise.any()

- **Returns the first fulfilled value**
- Ignores any rejected Promises
- If **all Promises reject**, it returns an `AggregateError`

```js


const p1 = new Promise((resolve, reject) => setTimeout(reject, 100, "❌ Failed from p1"));
const p2 = new Promise((resolve) => setTimeout(resolve, 100, "✅ Success from p2"));
const p3 = new Promise((resolve) => setTimeout(resolve, 200, "✅ Success from p3"));

Promise.any([p1, p2, p3])
  .then((res) => console.log(res)) // ✅ Success from p2
  .catch((err) => console.log(err));



```