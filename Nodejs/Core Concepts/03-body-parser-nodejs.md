# What is `body-parser` in Node.js?

`body-parser` is a middleware for Node.js used to parse incoming request bodies before your route handlers.

## 🔍 Why use it?

When a client sends data via `POST`, `PUT`, or `PATCH`, the data is in raw format.  
`body-parser` parses this data and makes it available on `req.body`.

## 🔧 Usage Example:

```js
const express = require('express');
const bodyParser = require('body-parser');
const app = express();

app.use(bodyParser.json()); // for parsing application/json
app.use(bodyParser.urlencoded({ extended: true })); // for parsing form data

app.post('/submit', (req, res) => {
  console.log(req.body);
  res.send('Data received');
});
```

## 📌 Built-in in Express 4.16+

You can use:

```js
app.use(express.json());
app.use(express.urlencoded({ extended: true }));
```

## 🧪 Parsers Summary:

| Middleware                  | Parses                                |
|----------------------------|----------------------------------------|
| `bodyParser.json()`        | JSON data                              |
| `bodyParser.urlencoded()`  | URL-encoded data from forms            |
| `bodyParser.text()`        | text data                              |
