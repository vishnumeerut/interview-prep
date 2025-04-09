# 🔁 Mutable vs Immutable in JavaScript

---

## 🧠 Definition

- **Mutable** objects can be **changed after creation**.
- **Immutable** objects **cannot be changed**—any update returns a **new copy** instead.

---

## ✅ Mutable Types

These can be **changed in-place**:

- Arrays
- Objects
- Functions

```js
let arr = [1, 2, 3];
arr.push(4); // ✅ modifies the original array
console.log(arr); // [1, 2, 3, 4]

let user = { name: "Vishnu" };
user.name = "Kumar"; // ✅ modifies the original object

```


## 🚫 Immutable Types

These cannot be changed, any operation **returns a new value**:
- Strings
- Numbers
- Booleans

```js
let str = "hello";
str[0] = "H"; // ❌ does nothing
console.log(str); // "hello"

let newStr = str.replace("h", "H");
console.log(newStr); // "Hello"


```