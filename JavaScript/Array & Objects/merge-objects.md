# 🧩 How to Merge Two Objects in JavaScript

Merging objects means combining the properties of two (or more) objects into one. This is commonly needed in JavaScript, especially when working with state, configs, or user data.

---

## ✅ Example Objects

```js

✅ Using Spread Operator (...)

const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const merged = { ...obj1, ...obj2 };
console.log(merged); // { a: 1, b: 3, c: 4 }

Note:- 🔁 Later values (obj2.b) override earlier ones (obj1.b)

```


```js

✅ Using Object.assign()

const obj1 = { a: 1, b: 2 };
const obj2 = { b: 3, c: 4 };
const merged = Object.assign({}, obj1, obj2);
console.log(merged); // { a: 1, b: 3, c: 4 }


Note:- 🔁 Later values (obj2.b) override earlier ones (obj1.b)

```