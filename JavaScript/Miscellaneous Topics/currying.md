# 🍛 Currying in JavaScript

---

## 🧠 What is Currying?

**Currying** is a mechanism/technique by which sequence of functions  with **multiple arguments** can be execute/evaluated.

> Instead of:  
> `f(a, b, c)`  
> You do:  
> `f(a)(b)(c)`

---

## 🧾 Why Use Currying?

✅ Reusability  
✅ Function composition  
✅ Partial application (pre-setting some arguments)  
✅ Cleaner, more readable code

---

## 🧪 Example: Curried Version

```js
function curriedAdd(a) {
  return function(b) {
    return a + b;
  };
}

console.log(curriedAdd(2)(3)); // 5

// You can reuse the first function
const addTwo = curriedAdd(2);
console.log(addTwo(10)); // 12

