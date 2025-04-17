# What is Middleware in Node.js?

In Express.js, **middleware** is a function that has access to the request (`req`) and response (`res`) objects, and the `next()` function in the application's request-response cycle.

### Features of Middleware:

- Executes any code
- Modifies `req` and `res` objects
- Ends the request-response cycle
- Calls the next middleware in the stack

### Syntax:

```js
function middleware(req, res, next) {
  // logic here
  next();
}
```

### Types of Middleware:

| Type              | Description |
|-------------------|-------------|
| Application-level | Defined using `app.use()` or `app.get()` |
| Router-level      | Attached to instances of `express.Router()` |
| Built-in          | Includes `express.static`, `express.json()` |
| Third-party       | Like `morgan`, `cors`, `body-parser` |
| Error-handling    | Has signature `(err, req, res, next)` |

### Example:

```js
const express = require('express');
const app = express();

// Custom middleware
function logger(req, res, next) {
  console.log(`${req.method} ${req.url}`);
  next();
}

app.use(logger);

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(3000, () => console.log("App is listining on port:- 3000"));
```

### Use Cases:

- Logging
- Authentication
- Input validation
- Error handling
- Serving static files

