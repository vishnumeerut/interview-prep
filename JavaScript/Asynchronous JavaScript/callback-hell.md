# 🔄 Callback Hell in JavaScript

---

## ❓ What is Callback Hell?

**Callback Hell** happens when multiple asynchronous operations are nested inside each other.  

It leads to:

- Deeply nested code,
- Hard-to-read and hard-to-maintain structure,
- Difficult debugging,

---

## 😖 Example: Callback Hell

```js
doTask1(() => {
  doTask2(() => {
    doTask3(() => {
      doTask4(() => {
        console.log("All tasks done!");
      });
    });
  });
});
```
## ✅ How to Avoid Callback Hell?

### 1. Use Promises
```js
doTask1()
  .then(doTask2)
  .then(doTask3)
  .then(doTask4)
  .then(() => console.log("All tasks done"))
  .catch((err) => console.error("Error:", err));
```


### 2. Use async/await (Best)

```js
async function runTasks() {
  try {
    await doTask1();
    await doTask2();
    await doTask3();
    await doTask4();
    console.log("All tasks done!");
  } catch (err) {
    console.error("Error:", err);
  }
}

runTasks();
```
