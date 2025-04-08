# 🧠 Difference Between `Object.keys()`, `Object.values()`, and `Object.entries()` in JavaScript

These three methods are used to work with the properties of an object.

---

## 🧪 Given Object:

```js
const user = {
  name: "Vishnu",
  city: "Meerut",
  role: "Software Developer"
};

🔑 Object.keys()
Returns an array of keys from the object.

const keys = Object.keys(user);
console.log(keys); 
// Output: ["name", "city", "role"]


🔢 Object.values()
Returns an array of values from the object.

const values = Object.values(user);
console.log(values); 
// Output: ["Vishnu", Meerut, "Software Developer"]

🪙 Object.entries()
Returns an array of key-value pairs (as arrays).

const entries = Object.entries(user);
console.log(entries);
/*
 Output: [  ["name", "Vishnu"], ["city", Meerut], ["role", "Software Developer"]  ]
*/

