# 🧠 What is Event Bubbling in JavaScript?

---

## 📖 Definition:

**Event Bubbling** is a type of event propagation in the DOM where an event **starts from the target element** and **bubbles up** to its ancestors (parent, grandparent, etc.).

---

## 🔄 Visual Example:

Suppose we click on a `<button>` inside a `<div>` which is inside a `<div>`:

```html
    <div id="parent" style="
    padding: 30px;
    background-color: #a0e7e5;
    border-radius: 15px;
    max-width: 600px;
    margin: 50px auto;

  ">
    Parent
  
    <div id="child" style="
      padding: 25px;
      background-color: #ffb997;
      border-radius: 12px;
      margin-top: 20px;

    ">
      Child
  

  
      <button id="btn" style="
        padding: 12px 20px;
        background-color: #6c63ff;
        color: white;
        border: none;
        border-radius: 8px;
        font-size: 16px;
        cursor: pointer;
        margin-top: 15px;
        margin-left: 15px;
        transition: background 0.3s ease;
      ">
        Click Me
      </button>
    </div>
  </div>

```


```js

        document.getElementById('parent').addEventListener('click', function (e) {
            console.log('Parent clicked');
        });
        
        document.getElementById("child").addEventListener("click", (e) => {
            console.log("Child Clicked..")
        })
        document.getElementById('btn').addEventListener('click', function (e) {
            console.log('Button clicked');
        });


🔄 Stop event bubling using event propogation

        document.getElementById('parent').addEventListener('click', function (e) {
            console.log('Parent clicked');
            e.stopPropagation()
        });
        
        document.getElementById("child").addEventListener("click", (e) => {
            console.log("Child Clicked..")
            e.stopPropagation()
        })
        document.getElementById('btn').addEventListener('click', function (e) {
            console.log('Button clicked');
            e.stopPropagation()
        });
```