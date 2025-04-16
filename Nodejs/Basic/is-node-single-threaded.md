# Is Node.js single-threaded? How does it handle multiple tasks at once?

## ✅ Yes, Node.js is single-threaded, but it handles multiple tasks using **asynchronous non-blocking I/O** and the **Event Loop**.

---

## 🧠 Explanation:

Although Node.js uses a single thread to run JavaScript code, it uses:

- **Event Loop** to handle asynchronous operations.
- **Callback Queue** to store and process completed tasks.
- **Worker Pool (libuv)** to handle I/O-intensive operations like file handling, networking, and encryption in the background.

---

## ⚙️ Behind the Scenes:

```text
Main Thread → Executes JavaScript code

Async Task → Sent to Worker Pool (e.g., file read)

Worker Pool → Processes in background

Event Loop → Pushes completed task callback to queue

Callback Queue → Executes the callback without blocking
```

---

## ✅ Result:
This architecture lets Node.js handle **thousands of concurrent connections** with high efficiency, despite being single-threaded.

---

## 🧠 Summary:
Node.js is single-threaded but uses **non-blocking I/O**, **event loop**, and **background threads** to manage concurrency.
