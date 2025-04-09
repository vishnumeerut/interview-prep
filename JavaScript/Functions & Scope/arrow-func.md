# 🏹 Arrow Function in JavaScript

## ✅ What is an Arrow Function?

An **arrow function** is a shorter syntax introduced in ES6 to write functions.  
It is best used for **concise one-liner functions**, especially in **callbacks** or **functional programming**.

---

## 🔁 Difference Between Normal Function and Arrow Function

| Feature                 | Normal Function                             | Arrow Function                                |
|-------------------------|----------------------------------------------|-----------------------------------------------|
| **Syntax**              | `function greet(name) {}`                   | `(name) => {}`                                |
| **`this` Binding**      | Dynamic (based on how it's called)          | Lexical (inherits from surrounding scope)     |
| **Constructor**         | ✅ Yes, can be used with `new`              | ❌ No, cannot be used as a constructor         |
| **`arguments` object**  | ✅ Available                                 | ❌ Not available                               |
| **Use Case**            | General functions, methods, constructors    | Callbacks, small utility functions            |

---

## 💻 Example: Basic Syntax

### 🔹 Arrow Function

```js

const greet = (name) => "Hello " + name;

console.log(greet("Vishnu")); // Hello Vishnu

```

### 🔹 Arrow Function with this
```js

const person = {
  name: "Vishnu",
  regularFunc: function () {
    console.log("Regular:", this.name);
  },
  arrowFunc: () => {
    console.log("Arrow:", this.name);
  },
};

person.regularFunc(); // Regular: Vishnu
person.arrowFunc();   // Arrow: undefined

