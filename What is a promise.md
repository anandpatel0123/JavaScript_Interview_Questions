Promise ek aisa object hai jo bhavishya mein kisi samay ek single value produce kar sakta hai, jise ya toh resolved value hota hai ya phir wajah hoti hai ki yeh resolved nahi hua (for example, network error). Yeh teeno possible states mein hoga: fulfilled, rejected, ya pending.

Promise banane ka syntax kuch is tarah ka hota hai,

```js
const promise = new Promise(function (resolve, reject) {
  // promise description
});
```

```js
const promise = new Promise(
  (resolve) => {
    setTimeout(() => {
      resolve("Main ek Promise hoon!");
    }, 5000);
  },
  (reject) => {}
);

promise.then((value) => console.log(value));
```

![[Promise Action Flow.png]]

### Why do you need a promise

```js
Promise ka istemal asynchronous operations ko handle karne ke liye hota hai. Yeh callback hell ko kam karke aur cleaner code likhne ka ek alternative approach provide karte hain.
```

### What are the three states of promise

1. **Pending:** Yeh ek Promise ka initial state hai, jab koi operation shuru hone se pehle hota hai.
2. **Fulfilled:** Yeh state yeh batata hai ki specific operation complete ho gaya hai.
3. **Rejected:** Yeh state yeh batata hai ki operation complete nahi hua. Is case mein ek error value throw ki jaati hai.
