# How to check an array  in javaScript



## 💻 Example Code:

1. **Array.isArray(variable)** Recommended 
   ```js
    const arr = [1, 2, 3];
    console.log(Array.isArray(arr)); // true
   ```

2. **instanceof operator**   
   ```js
    const arr = [1, 2, 3];
    console.log(arr instanceof Array); // true
   ```


3. **Object.prototype.toString.call(variable)**   
   ```js
   const arr = [1, 2, 3];
   console.log(Object.prototype.toString.call(arr).slice(8, -1)); // "Array"
   ```

    
