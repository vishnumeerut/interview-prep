# 🌐 What is CORS in JavaScript?

---

## ✅ What is CORS?

CORS stands for **Cross-Origin Resource Sharing**.  
It's a **security feature** implemented by browsers to prevent unauthorized access between different origins (domains, ports, or protocols).

---

## 🧠 What is an Origin?

An **origin** is made of:

- Protocol (http or https)
- Domain (example.com)
- Port (3000, 8000, etc.)

Two URLs are **cross-origin** if any one of these is different.

---

## ❌ CORS Error Example

When a JavaScript frontend (e.g., React on `localhost:3000`) tries to fetch data from a backend on `localhost:5000`, the browser **blocks** the request unless the backend explicitly allows it.


**Use a proxy server**: Dev tools like `vite`, `webpack`, or a custom proxy server can forward API requests.

```js
// In React setupProxy.js or vite.config.js
"/api": {
  target: "http://localhost:5000",
  changeOrigin: true
}


