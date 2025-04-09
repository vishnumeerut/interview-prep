# Callback Function in JavaScript.

## 🧠 Definition:

- `callback`: A callback function is a function passed as an argument to another function, and it's executed later, often after some operation completes.


## 💻 Example Code:


```js
function greetUser(name, callback) {
  console.log(`Hi ${name}`);
  callback(); // call the passed function
}

function sayBye() {
  console.log("Goodbye!");
}

// Passing sayBye as a callback
greetUser("Vishnu", sayBye);
