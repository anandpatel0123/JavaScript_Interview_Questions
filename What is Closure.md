## 1. What is Closure?

   jab ek function doosre function ke andar aata hai, toh ek closure ban jata hai. Closure outer variable ko yaad rakhta hai aur outer scope ke members ko access karne mein madad karta hai.

## 2. Simple Example Ke Saath Shuru Karte Hain:

   Ek simple example ke saath closure ka concept samjhte hain.

   **Example:**
   ```javascript
   const outer = () => {
       let innerVar = "Inner Card";
       const inner = () => {
           console.log(innerVar);
       };
       return inner;
   };

   const innerFn = outer();
   innerFn();  // Output: Inner Card
   ```

   Yahan `inner` function, `outer` function ke andar bani hai, aur closure ke roop mein `innerVar` ko yaad rakhti hai.

## 3. Closure Ke Fayde:

   Closure ka istemal karne se private members ko global taur par access kiya ja sakta hai, lekin dhyan rakhe ki iska istemal saavdhanipoorvak karna chahiye.

## 4. Advantages of Closure:


   **Example:**
   ```javascript
   const addCounter = () => {
       let counter = 0;
       const incrementCounter = () => {
           counter++;
           console.log(counter);
       };
       return incrementCounter;
   };

   const counter1 = addCounter();
   counter1();  // Output: 1
   counter1();  // Output: 2

   const counter2 = addCounter();
   counter2();  // Output: 1
   ```

   Yahan `counter` variable `addCounter` ke andar closure ke roop mein hai, jisse har bar `incrementCounter` ko call karne par `counter` badhata hai aur uski value yaad rakhta hai.

## 5. Related Questions:

### Q1. Closure Kaise Kaam Karta Hai?

   Closure kaam karte hain jab ek function doosre function ke andar hota hai aur woh outer function ke variables ko yaad rakhta hai.

### Q2. Closure Ka Istemal Kahan Aur Kaise Hota Hai?

   Closure ka istemal private members ko global level par access karne ke liye hota hai. Iska istemal tab hota hai jab aap kisi function ke andar ek aur function ko return karte hain.

### Q3. Closure Ka Istemal Karna Kab Aur Kyun Zaruri Hai?

   Closure ka istemal karna zaruri hai jab aap kuch private members ko global level par expose karna chahte hain, lekin dhyan rakhe ki iska istemal saavdhanipoorvak hona chahiye. Kabhi-kabhi closure ka istemal avoid bhi kiya ja sakta hai.
