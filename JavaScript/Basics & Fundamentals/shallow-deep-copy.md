## 🔹 Difference Between `shallow copy` and `deep copy`

### ✅ Definition

**`shallow copy`** Copies only the first level of an object. Nested objects still refer to the same memory.

**`deep copy`** Creates a complete independent clone of the object, including all nested structures...

### ✅ Example

### Shallow Copy

```js


    const original = { name: "John", address: { city: "NY" } };
    const shallow = { ...original };

    shallow.address.city = "LA";

    console.log(original.address.city); // "LA" - changed in original too!


    let b = null;
    console.log(b); // null

```

### Deep Copy

```js


    const original = { name: "John", address: { city: "NY" } };
    const shallow = { ...original };

    const deep = JSON.parse(JSON.stringify(original));
    deep.address.city = "Chicago";
    console.log(original.address.city); // "LA" → original remains unchanged

// Note:- It does not work with date object.
```
### Deep Copy with structuredClone

```js

    const original = { name: "John", address: { city: "NY" } };
    const deep = structuredClone(original);

    deep.address.city = "LA";

    console.log(original.address.city); // "NY" - original remains unchanged ✅

    // Note:- It works with date object too.
```


