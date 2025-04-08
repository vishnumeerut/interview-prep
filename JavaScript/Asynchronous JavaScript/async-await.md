# ⏳ async/await in JavaScript

---

## ✅ What is async/await?

`async/await` is **syntactic sugar** over Promises in JavaScript that allows you to write asynchronous code in a **synchronous-like** manner, making it easier to read and maintain.

- `async` makes a function return a **Promise**
- `await` pauses the function execution until the Promise is complete ( **fullfilled/rejected** )

---

## 🔧 Basic Example

```js
function waitForms(timeInms) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve()
        }, timeInms)
    })
}


async function greet () {
    console.log("Start");
    await waitForms(5000); // wait for 5 secs here...
    console.log("End!")
}

greet();
