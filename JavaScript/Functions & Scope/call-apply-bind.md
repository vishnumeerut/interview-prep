# 🧠 Understanding `call()`, `apply()`, and `bind()` in JavaScript

## ✅ Purpose

All three methods are used to **explicitly set the value of `this`** when calling a function..

---

## 📊 Comparison Table

| Method     | Calls Function? | Accepts Arguments?       | Returns What?              |
|------------|------------------|---------------------------|-----------------------------|
| `call()`   | ✅ Immediately    | Yes, passed **individually** | Return value of function    |
| `apply()`  | ✅ Immediately    | Yes, passed as an **array** | Return value of function    |
| `bind()`   | ❌ Not Immediately| Yes, passed individually    | ✅ Returns a new function    |

---

## 💻 Example Call

```js
const person = {
  name: "Vishnu",
};

function greet(greeting, punctuation) {
  console.log(`${greeting}, ${this.name}${punctuation}`);
}

greet.call(person, "Hello", "!"); // Hello, Vishnu!

```

## 💻 Example Apply

```js
const person = {
  name: "Vishnu",
};

function greet(greeting, punctuation) {
  console.log(`${greeting}, ${this.name}${punctuation}`);
}

greet.apply(person, ["Hi", "!!"]); // Hi, Vishnu!!

```
## 💻 Example Bind

```js
const person = {
  name: "Vishnu",
};

function greet(greeting, punctuation) {
  console.log(`${greeting}, ${this.name}${punctuation}`);
}

const greetVishnu = greet.bind(person, "Hey", "...");
greetVishnu(); // Hey, Vishnu...


```
