# 🧩 What is Event Delegation in JavaScript?

## ✅ Definition

**Event Delegation** is a technique in JavaScript where you **attach a single event listener to a parent element** instead of multiple listeners to individual child elements.

The event **bubbles up** from the child to the parent, and you can catch it using the parent’s listener.

---

## 🔍 Why Use Event Delegation?

- ✅ Better performance (especially for dynamic or many child elements)
- ✅ Less memory usage
- ✅ Clean, maintainable code

---

## 💡 Real-Life Example

Instead of adding a click event to each button:

```html
    <div id="grandparent">
        <div id="parent">
            <div id="child">
                <h1>Event Delegation</h1>
            </div>
        </div>
    </div>

```

```js

        document.getElementById("grandparent").addEventListener("click", (event) => {

            if(event.target.id == "child") {
                console.log("Child Clicked!")
            }
            else if (event.target.id == "parent") {
                console.log("Parent Clicked!")
            }
            else if (event.target.id == "grandparent"){
                console.log("Grand Parent Clicked!")
            }
        })
           
    /*
        document.getElementById("parent").addEventListener("click", (event) => {
            console.log("parent clicked...")
        })
        document.getElementById("grandparent").addEventListener("click", (event) => {
            console.log("grandparent clicked...")
        })
        document.getElementById("child").addEventListener("click", (event) => {
            console.log("child clicked...")
        })

     */
```
