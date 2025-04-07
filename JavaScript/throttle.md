# ⏱️ Throttling in JavaScript

## ✅ What is Throttling?

**Throttling** is a technique to **limit the number of times a function can be executed** over time.

It ensures that a function runs **at most once every X milliseconds**, no matter how often an event is triggered.

---

## 🧠 Why Use Throttling?

- To **improve performance** on frequently firing events like `button`, `mousemove`, `scroll`.
- To prevent a function from being called **too often** and slowing down your app.

---

## 💻 Code Example: Throttle 





```html
    <button onclick="throttleButton(event)">Click</button>



```

```js

        const buttonQuery = (event) => {
            console.log(`Button... ${event.target.textContent}`);
        }

        function throttle (fn, delay) {
            let lastCall = 0;
            return function (...args) {
                let now = Date.now();
                if(now - lastCall < delay) {
                    return;
                }
                lastCall = now;
                return fn(...args)
            }
        }

        const throttleButton = throttle(buttonQuery, 5000)
