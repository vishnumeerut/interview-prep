# Control Flow in Node.js

Control flow in Node.js refers to the **order in which statements are executed**, especially when dealing with **asynchronous operations** like reading files, accessing databases, or handling HTTP requests.

## 🔁 How it works:

1. Start an operation (like reading a file)
2. Provide a callback to execute when it's done
3. Continue executing next lines of code
4. Callback runs once the async operation completes

### Example:

```js
const fs = require('fs');

console.log("Start");

fs.readFile('example.txt', 'utf8', (err, data) => {
  if (err) throw err;
  console.log("File content:", data);
});

console.log("End");
```

**Output:**
```
Start
End
File content: <file data>
```

## 🔄 Control Flow Techniques:

| Technique        | Description                                |
|------------------|--------------------------------------------|
| Callbacks        | Traditional way to manage async logic      |
| Promises         | Better syntax to handle async flow         |
| Async/Await      | Cleaner, readable code with async functions|
| Event Emitters   | Used for handling custom async events      |
| Middleware Stack | Express uses chained middleware functions  |

## ✅ Benefits:

- Non-blocking execution
- Efficient I/O handling
- Better performance in handling concurrent operations

