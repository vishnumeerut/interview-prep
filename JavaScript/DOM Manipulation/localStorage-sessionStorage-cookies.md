# 🗂️ Difference Between localStorage, sessionStorage, and cookies

---

## 📘 Overview

| Feature            | `localStorage`                 | `sessionStorage`               | `cookies`                       |
|--------------------|---------------------------------|--------------------------------|---------------------------------|
| Lifespan           | Until manually deleted          | Until tab/window is closed     | Set by expiry date or session  |
| Storage Limit      | ~5MB                            | ~5MB                            | ~4KB                            |
| Sent with Requests | ❌ No                           | ❌ No                           | ✅ Yes (automatically sent)     |
| Accessibility      | `client-side only`              | `client-side only`             | `client + server`              |
| Use Case           | Persistent login, settings      | Tab-specific data              | Auth/session management         |

---

## 📦 localStorage

- Stores data with **no expiration**
- Shared across all tabs/windows from the same origin
- Useful for settings, themes, tokens

```js
localStorage.setItem("name", "Vishnu");
console.log(localStorage.getItem("name")); // Vishnu
localStorage.removeItem("name");
localStorage.clear();
```

## 📦 sessionStorage

- Similar to localStorage but only available for the current tab/session
- Gets cleared automatically when tab is closed

```js
sessionStorage.setItem("auth", "true");
console.log(sessionStorage.getItem("auth")); // true
sessionStorage.clear();

```

## 🍪 cookies

- Small pieces of data sent with every HTTP request
- Can be used for both client- and server-side
- Supports `expires`, `path`, `secure`, and `httpOnly` flags

```js

document.cookie = "username=Vishnu; expires=Fri, 31 Dec 2025 23:59:59 UTC; path=/";
console.log(document.cookie); // username=Vishnu


```