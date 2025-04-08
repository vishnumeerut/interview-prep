# 🔍 How `querySelectorAll()` Works in JavaScript

---

## ✅ Definition

`document.querySelectorAll()` returns a **NodeList** of **all elements** that match a specified **CSS selector**.

---

## 🧠 Syntax

```html 
<ul>
  <li class="item">Apple</li>
  <li class="item">Banana</li>
  <li class="item">Cherry</li>
</ul>
```

```js

// Syntax
document.querySelectorAll(selector);

const items = document.querySelectorAll(".item");

items.forEach((item) => {
  console.log(item.textContent);
});

```
