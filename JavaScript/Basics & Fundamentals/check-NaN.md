
# NaN in JavaScript


## 🧠 Definition:


- `NaN` :->  NaN stands for **Not-a-Number**.
- It is a special value in JavaScript used to represent a value that is not a valid number.
- It is of type number, but it is not equal to any number, including itself...



## 💻 Example Code:


### How to check if a value is NaN?

1. **Using isNaN()** 

- Converts the value to a number and checks if the result is NaN.
   ```js
   isNaN("hello") // true (not reliable for strict checking)
   ```

2. **Using Number.isNaN()** – Recommended 

- Checks if the value is exactly `NaN` without type coercion.
   ```js
    Number.isNaN(NaN); // true
    Number.isNaN("hello"); // false
   ```







