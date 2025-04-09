# 📦 What is Dynamic Import in JavaScript?

---

## ✅ Definition

**Dynamic import** allows you to **load JavaScript modules dynamically at runtime** using the `import()` function instead of static `import` statements.

Unlike regular `import`, which happens at the top and loads all modules when the app starts, dynamic `import()` lets you load code only **when you need it** — saving resources and improving performance.

---

## 🔧 Syntax

```js
import("module-path")
  .then((module) => {
    // Use the module
  })
  .catch((error) => {
    console.error("Failed to load module:", error);
  });
