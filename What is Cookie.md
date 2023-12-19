Cookie ek chhota sa data hai jo aapke computer mein store ho jaata hai aur jise aapke browser access karta hai. Cookies ko key/value pairs ke roop mein save kiya jaata hai.

```js
document.cookie = "username=John";
```
### Why do you need a Cookie

Cookies ka istemal user ke profile (jaise ki username) ke baare mein jaankari yaad rakhne ke liye hota hai. Yeh basically do tarah se hota hai,

1. Jab user kisi web page ko visit karta hai, toh uske profile ka data ek cookie mein store ho jaata hai.
2. Jab agli baar user wahi page visit karta hai, toh cookie us user ke profile ko yaad rakhta hai.

### What are the options in a cookie

- By default, cookie browser band hone par delete ho jaata hai, lekin aap isko expiry date set karke badal sakte hain.

```js
document.cookie = "username=John; expires=Sat, 1 Jan 2024 12:00:00 UTC";
```

By default, cookie current page se belong karta hai. Lekin aap path parameter ka istemal karke browser ko bata sakte hain ki cookie kis path se belong karta hai.

```js
document.cookie = "username=John; path=/services";
```

### How do you delete a cookie

Aap ek cookie ko delete kar sakte hain by setting expiry date ko ek pehle se passed date. Is case mein aapko cookie value specify karne ki zarurat nahi hoti. For example, aap current page par ek username cookie ko is tarah se delete kar sakte hain,

```js
document.cookie = "username=; expires=Mon, 01 Jan 2024 00:00:00 UTC; path=/;";
```

****Note**** Aapko cookie ko sahi tarah se delete karne ke liye cookie path option define karna chahiye. Kuch browsers cookie ko delete karne ki permission nahi dete agar aap path parameter specify nahi karte to.
