**Undefined:** Undefined hota hai jab kisi variable ko value assign nahi ki gayi hoti. Matlab, variable declare toh kiya hai, lekin usme koi value assign nahi hui hai.

```js
let naam; // yaha pe variable declare karte time koi type decide nahi hai, jis wajah se undefined hai
console.log(naam); // Output: undefined
console.log(typeof naam) // undefined

// Yahi agar hum value assign karte hai to usko type mil jayega
naam = 10 // number type mil gya
console.log(naam) // Output: 10
console.log(typeof naam) // number
```

***Null:*** Null hota hai jab explicitly kisi variable ko koi value nahi milti, ya fir hum chahte hain ki uss variable ka value null ho.
*Null means nothing***

```js
let umar = null;
console.log(umar); // Output: null
```

Questions Related to above topic: 

1. ***What is undefined in JavaScript?***
A variable which is not assigned a value is undefined

2. ***What will be the output of `undefined == null` and `undefined===null`***
`undefined==null`--> true
`undefined===null` --> false

3. ***Can you explicitly assign undefined to a variable?***
Yes

