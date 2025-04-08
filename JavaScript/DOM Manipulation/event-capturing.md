# 🔄 What is Event Capturing in JavaScript?

---

## 📖 Definition

**Event Capturing** (also known as **capture phase**) is the **first phase** of event propagation in the DOM.

When an event is triggered, it goes through three phases:
1. **Capturing Phase** – from `window` down to the target element
2. **Target Phase** – the actual target element
3. **Bubbling Phase** – bubbles up from target to its ancestors

So, capturing happens **before** bubbling.

---

## 📦 Visual Flow



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
            
        }, true);
        
        document.getElementById("child").addEventListener("click", (e) => {
            console.log("Child Clicked..")
        }, true)
        
        document.getElementById('btn').addEventListener('click', function (e) {
            console.log('Button clicked');
        }, true);

