# ❓ Optional Chaining (`?.`) in JavaScript

---

## ✅ What Is Optional Chaining?

Optional chaining (`?.`) is a **safe way to access nested object properties** without worrying about runtime errors if a property doesn't exist.

> Instead of throwing an error, it returns `undefined`.

---

## 🔧 Syntax

```js
object?.property
object?.[expression]
object?.method?.()
```

### 💥 Without Optional Chaining (Error-prone)
```js
const user = {};
console.log(user.address.city); // ❌ Error: Cannot read property 'city'
```


### ✅ With Optional Chaining (Safe)
```js
const user = {};
console.log(user.address?.city); // ✅ undefined (no crash)
```

### 🛠️ Real-World Example
```js
const user = {
  name: "Vishnu",
  contact: {
    email: "vishnu@example.com",
  }
};

console.log(user.contact?.email); // ✅ vishnu@example.com
console.log(user.contact?.phone); // ✅ undefined
console.log(user.address?.city);  // ✅ undefined

```

### 📞 With Method Calls
```js
const user = {
  sayHi() {
    return "Hello!";
  }
};

console.log(user.sayHi?.()); // ✅ "Hello!"
console.log(user.sayBye?.()); // ✅ undefined (no error)

```