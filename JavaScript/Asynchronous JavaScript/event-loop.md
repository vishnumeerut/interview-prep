# 🔄 What is the Event Loop in JavaScript?

---

## ✅ Definition

The **Event Loop** is a core part of the JavaScript runtime that handles **asynchronous operations** like:

- `setTimeout`
- `Promises`
- `DOM Events`
- `fetch calls`

JavaScript is **single-threaded**, so the event loop allows it to handle multiple tasks **non-blockingly**.

---

## 🧠 How It Works (In Simple Words)

1. All **synchronous code** runs in the **Call Stack**
2. Async operations go to the **Web APIs** (like `timers`, `fetch`, etc.)
3. Once done, their callbacks go to the **Callback Queue** or **Microtask Queue**
4. The **Event Loop** checks:
   - If the **Call Stack** is empty
   - Then pushes the next task from the queue into the Call Stack

---

## 🔄 Visual Flow

```text
       ┌────────────────────────────┐
       │        Call Stack          │
       └────────────┬───────────────┘
                    │
                    ▼
       ┌────────────────────────────┐
       │        Web APIs            │
       └────────────┬───────────────┘
                    ▼
       ┌────────────┴───────────────┐
       │     Callback / Task Queue  │
       └────────────┬───────────────┘
                    │
                    ▼
       ┌────────────────────────────┐
       │        Event Loop          │
       └────────────────────────────┘
```

```js
console.log("1");

setTimeout(() => {
  console.log("2");
}, 0);

Promise.resolve().then(() => {
  console.log("3");
});

console.log("4");
// Output:-  1, 4, 3, 2
```
`Promise` goes to the **Microtask queue**

`setTimeout` goes to the **Callback queue / Macrotask queue**

`Microtasks` are executed before `Callback queue` due to high priority.

