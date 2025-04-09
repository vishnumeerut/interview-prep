# 🔹 JavaScript all Data Types. 


## ✅ Primitive Data Types 

1. **String** – Text data  
   ```js
   let name = "Alice";
   ```

2. **Number** – Integer or floating point  
   ```js
   let age = 25;
   ```

3. **Boolean** – `true` or `false`  
   ```js
   let isActive = true;
   ```

4. **Undefined** – Variable declared but not assigned  
   ```js
   let x;
   ```

5. **Null** – Explicit absence of value  
   ```js
   let data = null;
   ```

6. **BigInt** – Large integers  
   ```js
   let big = 1234567890123456789012345678901234567890n;
   ```

7. **Symbol** – Unique and immutable value  

> To create unique keys in objects..

   ```js
    const id1 = Symbol("userId");
    const id2 = Symbol("userId");

    console.log(id1 === id2); // false (Symbols are always unique)

    const user = {
    name: "Alice",
    [id1]: 101,
    [id2]: 102
    };

    console.log(user[id1]); // 101
    console.log(user[id2]); // 102




