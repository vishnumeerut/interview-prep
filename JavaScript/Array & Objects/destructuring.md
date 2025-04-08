# 📦 JavaScript Destructuring (ES6)

**Destructuring** is a shorthand syntax that lets you unpack values from arrays or properties from objects into distinct variables.

---

## 📚 1. Array Destructuring

### ✅ Basic Example

```js
const fruits = ["apple", "banana", "mango"];
const [a, b, c] = fruits;

console.log(a); // "apple"
console.log(b); // "banana"
console.log(c); // "mango"


✅ Skipping Elements

const [first, , third] = fruits;
console.log(first); // "apple"
console.log(third); // "mango"


✅ With Default Values

const [x, y, z = "orange"] = ["grape", "kiwi"];
console.log(z); // "orange"
```



## 📚 2. Object Destructuring

### ✅ Basic Example

```js
const person = {
  name: "Vishnu",
  work: "Software Engineer",
  city: "Meerut"
};

const { name, city } = person;

console.log(name); // "Vishnu"
console.log(city);  // Software Engineer



✅ Renaming Variables

const { name: userName } = person;
console.log(userName); // "Vishnu"



✅ With Default Values

const { country = "India" } = person;
console.log(country); // "India"

```

