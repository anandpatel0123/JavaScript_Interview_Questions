**Positive Infinity vs Negative Infinity**

**Positive Infinity (`Infinity`):**

JavaScript mein, `Infinity` ek mathematical concept ko represent karta hai. Ye ek aisi value hai jo ki kisi bhi aur numeric value se badi hoti hai. Jab koi numeric calculation JavaScript mein maximum number se bhi bada result deta hai, to wo result `Infinity` ke roop mein dikhai deta hai.

```js
console.log(Number.POSITIVE_INFINITY);

console.log(9e4); // 9 * 10^4
console.log(9e400);
console.log(Number.MAX_VALUE*2);
console.log(1/0)
```


**Negative Infinity (`-Infinity`):**

Saath hi, JavaScript mein negative infinity ko bhi represent kiya gaya hai, jo ki `-Infinity` hota hai. Negative infinity bhi ek aisi value hai jo ki kisi bhi aur numeric value se chhoti hoti hai.

```js
console.log(Number.NEGATIVE_INFINITY);

console.log(-9e400);
console.log(-Number.MAX_VALUE*2);
```

**Questions related to Positive Infinity vs Negative Infinity:**

1. ***JavaScript mein Infinity kya hai?***
   - `Infinity` ek positive infinity ko darust karne wala mathematical concept hai, jo kisi bhi aur numeric value se bada hota hai.

2. ***Negative Infinity ko JavaScript mein kaise represent kiya gaya hai?***
   - Negative infinity ko `-Infinity` ke roop mein darust kiya gaya hai, jo ki kisi bhi aur numeric value se chhoti hoti hai.

3. ***Kya mathematical operations se Infinity hasil ho sakta hai?***
   - Haan, jab kuch calculations JavaScript mein maximum representable numeric value ko paar kar deti hain, to unhe `Infinity` ke roop mein darust kiya jata hai.

4. ***`Infinity === -Infinity` aur `typeof Infinity` ka output kya hoga?***
   - `Infinity === -Infinity` ka output `false` hoga.
   - `typeof Infinity` ka output `'number'` hoga
   - `Infinity` ko numeric value maana jata hai.

****
