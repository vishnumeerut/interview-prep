# 🤔 Nullish Coalescing Operator (`??`) in JavaScript

---

## ✅ What Is Nullish Coalescing?

The **nullish coalescing operator (`??`)** returns the **right-hand operand** only if the **left-hand operand is `null` or `undefined`**.

> It’s like a smarter version of `||` that doesn’t treat `0`, `-0 `false`, or `''` as “empty”.

---

## 🔧 Syntax

```js
let result = value ?? fallback;


console.log(0 || "Vishnu") // Vishnu
console.log(0 ?? "Vishnu") // 0
```

## ⚖️ `??` vs `||`

| Expression             | `||` Result     | `??` Result    |
|------------------------|------------------|----------------|
| `"" || "default"`      | `"default"`      | `""`           |
| `0 || 5`               | `5`              | `0`            |
| `false || true`        | `true`           | `false`        |
| `null || "x"`          | `"x"`            | `"x"`          |
| `undefined || "x"`     | `"x"`            | `"x"`          |


✅ || checks for `falsy values`.
✅ ?? checks only for `null` or `undefined`.
