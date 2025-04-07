
# ⚡ Debouncing in JavaScript

## 🧠 Why Use Them?

To **optimize performance** when dealing with high-frequency events like:
- `scroll`
- `resize`
- `keyup/input`
- `mousemove`

---

## 🔁 Debouncing

### ✅ What is Debouncing?

Debouncing means **delaying the function execution** until a certain time has passed **after the last event**.  
Useful for operations that should only happen **once the user stops typing**.




## 💻 Example Code:


```html
    <input id="inp" type="text" placeholder="Enter Your Text here..." onkeyup="debouncedSearchQuery(event)">


```

```js

        const searchQuery = (event) => {
            console.log(`Searching for... ${event.target.value}`)
        }

        function debounce (fn, delay) {
            let timerId;
            return function (...args) {
                clearTimeout(timerId)
                 timerId = setTimeout(() => {
                    fn(...args)
                }, delay)
            }
        }

        const debouncedSearchQuery = debounce(searchQuery, 1000)