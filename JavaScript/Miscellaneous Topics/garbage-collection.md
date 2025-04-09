# 🗑️ Garbage Collection in JavaScript

---

## 🧠 What Is Garbage Collection?

Garbage Collection (GC) is the process of **automatically freeing up memory** that is no longer needed by the program.  
JavaScript has **automatic memory management**, which means developers don't need to manually allocate or free memory.

---

## 📦 How It Works?

JS uses a concept called **Reachability**:

> If a value is **reachable**, it’s in use and cannot be garbage collected.  
> If a value becomes **unreachable**, the garbage collector removes it from memory.

---

## 🌳 Root References (Always Reachable)

- Global variables
- Local variables in current function call
- Variables referenced in closures

Any object that is **reachable from these roots** is safe.

---

## ♻️ JavaScript Garbage Collection Algorithm

### ✅ Most modern JS engines (like V8) use:
- **Mark-and-Sweep Algorithm**

### Steps:
1. `"Mark"` all root references
2. `"Sweep"` through memory and remove all unmarked (unreachable) values

---

## 🧪 Example

```js
let user = {
  name: "Vishnu"
};

user = null; // Object is no longer reachable

// Garbage Collector will remove { name: "Vishnu" } from memory
