# 🔍 Difference Between innerHTML, innerText, and textContent

When working with DOM elements in JavaScript, we often need to access or update their content.  
Here’s how `innerHTML`, `innerText`, and `textContent` are different:

---

## 📊 Comparison Table

| Property       | Description                                                       | Returns Hidden Text | Includes HTML Tags | Read Performance |
|----------------|-------------------------------------------------------------------|----------------------|---------------------|------------------|
| `innerHTML`    | Gets or sets HTML content (including tags)                       | ❌ No                | ✅ Yes               | ❌ Slower         |
| `innerText`    | Gets or sets *visible* text (honors CSS styles like `display`)   | ❌ No                | ❌ No                | ✅ Medium         |
| `textContent`  | Gets or sets all text content (ignores styling & hidden elements)| ✅ Yes               | ❌ No                | ✅ Fastest        |

---

## 💻 Examples

### HTML

```html
<div id="example">
  <p style="display: none;">Hidden</p>
  <span>Hello <strong>World</strong></span>
</div>
```

```js
const el = document.getElementById("example");

console.log(el.innerHTML);
// "<p style="display: none;">Hidden</p><span>Hello <strong>World</strong></span>"

console.log(el.innerText);
// "Hello World"

console.log(el.textContent);
// "\n  Hidden\n  Hello World"
