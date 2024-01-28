# Arrow Functions

## 1. Arrow Functions Ka Functional Behavior:

   Arrow functions mein `this` object ka vyavahar thoda alag hota hai. Isme 'arguments' object ka support nahi hota aur 'new' keyword ke sath use nahi hota.

## 2. Syntax:

### Traditional Function Syntax:

   Isey function keyword ka istemal karke functions ko define karte hai

   **Example:**
   ```javascript
   function add(a, b) {
       return a + b;
   }
   ```

### Function Expression:

   Isme var ya const ka istemal karke function expressions ko define karte hai:
   
   **Example:**
   ```javascript
   const add = function(a, b) {
       return a + b;
   };
   ```

### Arrow Functions:

   Isme arrow (=>) ka istemal function expressions ko chhota banane ke liye hota hai.

   **Example:**
   ```javascript
   const addArrow = (a, b) => a + b;
   ```

## 3. Arrow Function Ke Parameters:

   Arrow functions mein parameters ke liye parentheses ka istemal hota hai, lekin ek hi parameter ke liye unka istemal optional hota hai.

   **Examples:**
   ```javascript
   // With parentheses
   const greet = (name) => console.log("Hello, " + name);

   // Without parentheses
   const greetSingle = name => console.log("Hello, " + name);
   ```

## 4. Single-Line Arrow Functions:

   Single-line arrow functions ke liye curly braces aur 'return' likhne ki zarurat nahi hoti, jo ki syntax ko aur bhi sanchit bana deta hai.

   **Example:**
   ```javascript
   const square = x => x * x;
   ```

## 5. Functional examples:

### Simple Arrow Function:

   **Example:**
   ```javascript
   const greet = name => console.log("Hello, " + name);
   ```

### Optional Parentheses:

   Ek hi parameter ke liye parentheses ka istemal na karke arrow function ka udaharan.

   **Example:**
   ```javascript
   const greetSingle = name => console.log("Hello, " + name);
   ```

### Rest Parameters ke Sath Arguments Handling:

   Arrow functions mein 'arguments' object nahi hota, iske badle mein rest parameters ka istemal hota hai.

   **Example:**
   ```javascript
   const sum = (...args) => args.reduce((acc, val) => acc + val, 0);
   ```

#### Immediately Invoked Function Expression (IIFE):

   Arrow functions ka istemal IIFE banane ke liye kaise hota hai, jo ki turant execute hota hai.

   **Example:**
   ```javascript
   (() => {
       console.log("IIFE using Arrow Function");
   })();
   ```

## 6. Considerations Aur Limitations:

### `this` Object Arrow Functions Mein:

   Yeh samjhaata hai ki `this` object arrow functions mein traditional functions ke comparison mein kaise alag hota hai.

   **Example:**
   ```javascript
   const obj = {
       name: "John",
       greet: () => {
           console.log("Hello, " + this.name);  // 'this' does not refer to obj
       }
   };
   ```

### `arguments` Object Arrow Functions Mein:

   Yeh batata hai ki arrow functions mein traditional `arguments` object ka support kyun nahi hota aur iske badle mein rest parameters ka istemal kyun karna chahiye.

   **Example:**
   ```javascript
   const exampleArrow = (...args) => {
       console.log(args);
   };
   ```

## 7. Related Questions:

### Q1. Arrow functions aur traditional functions mein kya difference hai?

   Arrow functions syntax mein chhote hote hain aur 'this' keyword ke behaviour mein antar hota hai. Traditional functions mein 'this' dynamically bind hota hai, lekin arrow functions mein lexical scope ke hisab se bind hota hai.

### Q2. Arrow functions mein 'arguments' object kyun nahi hota?

   Arrow functions ke andar 'arguments' object ka istemal nahi hota, kyunki yeh dynamic 'this' keyword ke sath conflict karta hai. Rest parameters ka istemal arrow functions mein iske ek alternative ke taur par hota hai.

### Q3. Kya arrow function mein 'return' likhna zaruri hai?

   Agar arrow function ek hi statement return kar rahi hai, toh 'return' likhne ki zarurat nahi hai. Multiple statements ho toh curly braces aur 'return' ka istemal karna padta hai.
