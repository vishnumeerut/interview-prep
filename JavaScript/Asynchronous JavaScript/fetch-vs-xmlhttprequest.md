# 🌐 Fetch API vs XMLHttpRequest

---

## 1. ✅ Fetch API

`fetch()` is a modern way to make HTTP requests in JavaScript. It returns a **Promise** and is simpler and cleaner than older methods.

### 🔧 Example:

```js
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then((res) => res.json())
  .then((data) => console.log("📦 Data:", data))
  .catch((err) => console.error("❌ Error:", err));
```



## 2. 🕰 XMLHttpRequest 

`XMLHttpRequest()` (XHR) is an older method to send and receive data from a server. It doesn't use Promises and requires more code.

### 🔧 Example:

```js
const xhr = new XMLHttpRequest();
xhr.open("GET", "https://jsonplaceholder.typicode.com/posts/1");

xhr.onload = function () {
  if (xhr.status === 200) {
    const data = JSON.parse(xhr.responseText);
    console.log("📦 Data:", data);
  } else {
    console.error("❌ Request failed");
  }
};

xhr.onerror = function () {
  console.error("❌ Network Error");
};

xhr.send();

```