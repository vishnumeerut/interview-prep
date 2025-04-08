# 🔄 Different Ways to Iterate Over an Array in JavaScript

JavaScript provides multiple ways to loop through an array. Each has its own use case depending on what you're trying to do...

---

## 🧾 Example Array



## 🧾 For loop ( Classic )
```js
const fruits = ["apple", "banana", "mango"];
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
```


## 🧾 For...of loop 
```js
const fruits = ["apple", "banana", "mango"];
for (let fruit of fruits) {
  console.log(fruit);
}

```


## 🧾 forEach Method 
```js
const fruits = ["apple", "banana", "mango"];
fruits.forEach(function (fruit, index) {
  console.log(index, fruit);
});

```


## 🧾 Map Method 
```js
const fruits = ["apple", "banana", "mango"];
const upperFruits = fruits.map(fruit => fruit.toUpperCase());
console.log(upperFruits); // ['APPLE', 'BANANA', 'MANGO']
```


## 🧾 for...in loop
```js
const fruits = ["apple", "banana", "mango"];
for (let index in fruits) {
  console.log(index, fruits[index]);
}

```

## 🧾 while loop
```js
const fruits = ["apple", "banana", "mango"];
let i = 0;
while (i < fruits.length) {
  console.log(fruits[i]);
  i++;
}


```

## 🧾 do...while loop
```js
const fruits = ["apple", "banana", "mango"];
let i = 0;
do {
  console.log(fruits[i]);
  i++;
} while (i < fruits.length);


```