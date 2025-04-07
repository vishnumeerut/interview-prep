# 🔄 Synchronous vs Asynchronous Programming in JavaScript

## ❓ What’s the Difference?

| Feature              | Synchronous                           | Asynchronous                          |
|----------------------|----------------------------------------|----------------------------------------|
| **Execution**        | One task at a time, in order          | Tasks can run in the background       |
| **Blocking**         | ✅ Blocks next task until done         | ❌ Doesn’t block next task             |
| **Example**          | Simple math, loops                    | API calls, setTimeout, file reading   |
| **Speed**            | Slower if task takes time             | Faster and smoother for heavy tasks   |
| **User Experience**  | UI can freeze                         | Better user experience                |

---

## 💻 Code Examples

### 🔹 Synchronous Example:

```js
console.log("Start");
console.log("Middle");
console.log("End");

``` 

### 🔹 Asynchronous Example:

```js
console.log("Start");

setTimeout(() => {
  console.log("Middle");
}, 2000);

console.log("End");

