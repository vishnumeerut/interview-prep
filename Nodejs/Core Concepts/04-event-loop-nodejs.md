# 🔄 What is the Event Loop in Node.js?

Node.js uses the **event loop** to handle asynchronous operations like file I/O, network requests, and timers without blocking the main thread.

## 🧠 Key Concept

Even though Node.js is single-threaded, the **event loop** allows it to perform **non-blocking** tasks using background threads and callbacks.

## 🧱 How It Works

1. Code runs on the **call stack**.
2. Async operations are handled by **Web APIs**.
3. Completed tasks' callbacks go into the **callback queue**.
4. The **event loop** moves them back into the call stack when it is empty.



## 📊 Diagram

```
      ┌──────────────────────────┐
      │      call stack          │
      └──────────────────────────┘
                ▲
                │
       ┌────────┘
       │
┌──────────────┐       async task complete     ┌────────────────────┐
│  Web APIs    ├──────────────────────────────▶│  Callback Queue     │
└──────────────┘                                └────────────────────┘
                    ▲                                 │
                    │                                 ▼
                    └──────────────────────────┬──────┘
                                               ▼
                                        ┌─────────────┐
                                        │ Event Loop  │
                                        └─────────────┘

```

The event loop ensures Node.js handles multiple operations without blocking.
