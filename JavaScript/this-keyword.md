# 🔍 Understanding `this` Keyword in JavaScript

## ✅ What is `this`?

In JavaScript, `this` refers to the **context in which a function is called**.  
It can refer to **different values** depending on **how** and **where** the function is used.

---

## 📊 Behavior of `this` in Different Contexts

| Context                      | What `this` Refers To                                      |
|------------------------------|-------------------------------------------------------------|
| Global Scope (non-strict)    | Global object (`window` in browser, `global` in Node.js)   |
| Inside a Method              | The object calling the method                              |
| Inside a Function (strict)   | `undefined`                                                |
| Inside a Function (non-strict)| Global object                                              |
| In Arrow Function            | Inherits `this` from surrounding (lexical) scope           |
| In Constructor               | The newly created object                                   |
| In Event Listeners           | The DOM element that triggered the event                   |

---

## 💻 Examples

### 🔹 Global Scope

The value of this is replaceable by window object in non-strict mode.
due to **this substitution** algorithm.


```js
console.log(this); // In browser: window

```

### 🔹 Inside an Object Method

```js
const user = {
  name: "Vishnu",
  greet: function () {
    console.log("Hi, I'm " + this.name);
  },
};

user.greet(); // Hi, I'm Vishnu
```


### 🔹 Inside a Regular Function

```js
function show() {
  console.log(this);
}

show(); // In non-strict mode: window (or global), strict mode: undefined

```


### 🔹 Inside a Arrow Function

```js
const person = {
  name: "Vishnu",
  greet: () => {
    console.log("Hi, I'm " + this.name);
  },
};

person.greet(); // Hi, I'm undefined (arrow functions don't bind their own `this`)


```
### 🔹 Inside Constructor Function

```js
function Car(model) {
  this.model = model;
}

const myCar = new Car("Toyota");
console.log(myCar.model); // Toyota



```

