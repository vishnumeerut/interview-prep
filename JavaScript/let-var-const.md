# What is the difference between let, var, and const?

## 🧠 Definition:

- `var`: Function-scoped, can be redeclared and updated.
- `let`: Block-scoped, can be updated but not redeclared in the same scope.
- `const`: Block-scoped, cannot be updated or redeclared.

## 💻 Example Code:

### 🔁 Redeclare vs Reinitialize in JavaScript

#### ✅ Redeclare (Declaring the same variable again in the same scope)

```js
var a = 10;
var a = 20; // ✅ Allowed (redeclared with var)

let b = 10;
let b = 20; // ❌ Error (can't redeclare with let)

const c = 10;
const c = 20; // ❌ Error (can't redeclare with const)



var a = 10;
a = 20; // ✅ Allowed

let b = 10;
b = 20; // ✅ Allowed

const c = 10;
c = 20; // ❌ Error (can't reinitialize a const)


