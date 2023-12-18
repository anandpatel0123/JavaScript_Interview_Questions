There are many ways to create objects in javascript as mentioned below:

1. **Object literal syntax:**

   **Object literal** syntax ek simple tareeka hai object banane ka. Yeh ek set hai name-value pairs ka jo curly braces mein wrapped hota hai.

```js
    var vyakti = {
    naam: "John",
    umar: 28,
    shauk: ["reading", "coding"],
    pata: {
        sheher: "New York",
        zip: 10001
    },
    sayHello: function() {
        console.log("Hello from " + this.naam + "!");
    }
};

// Properties access aur method call
console.log(vyakti.naam); // Output: John
vyakti.sayHello(); // Output: Hello from John! 
```

    **Note:** Ye ek bahut hi aasan tareeka hai object banane ka.
    
2. **Object constructor:**

    Object constructor se empty object banane ka sabse seedha tareeka hai. Lekin abhi yeh approach recommended nahi hai.

    ```js
    var gaadi = new Object();
	gaadi.make = "Toyota";
	gaadi.model = "Camry";
	gaadi.year = 2022;
	
	console.log(gaadi.model); // Output: Camry
    ```

    `Object()` ek built-in constructor function hai, isliye "new" keyword ki zarurat nahi hai. Upar ka code iss tarah se likha ja sakta hai:

    ```js
    var object = Object();
    ```

3. **Object's create method:**
    
    Object's create method se new object create kar sakte hain by passing prototype object aur properties as arguments. Yeh pattern existing objects se new objects create karne mein madad karta hai.

    ```js
    var janwar = {
    prakar: "Kutta",
    awaz: "Woof!"
	};
	var kutta = Object.create(janwar);
	kutta.name = "Buddy";
	
	console.log(kutta.awaz); // Output: Woof!
    ```

4. **Function constructor:**

    Is approach mein, koi bhi function create karo aur use new operator se object instances bana sakte hain.

    ```js
    function Kitab(title, author) {
	    this.title = title;
	    this.author = author;
	}
	
	var meriKitab = new Kitab("The Ramayana", "Tulsidas");
	
	console.log(meriKitab.title); // Output: The Ramayana
    ```

5. **Function constructor with prototype:**

    Yeh function constructor ke similar hai lekin isme properties aur methods ke liye prototype ka use hota hai.
    JavaScript mai sabhi functions mai `prototype` property hoti hai, jiski madad se hum properties and methods add kar sakte hai. 
    Lekin jitne bhi instance banaye honge is constructor function ki help se, un sabhi mai ye properties add ho jayngi. 

    ```js
    function Film() {}
	Film.prototype.title = "Inception";
	Film.prototype.director = "Christopher Nolan";
	
	var inception = new Film();
	
	console.log(inception.director); // Output: Christopher    Nolan
    ```

6. **ES6 Class syntax:**
    
    ES6 ne class feature introduce kiya hai objects banane ke liye.

    ```js
    class Vahan {
	    constructor(make, model) {
	        this.make = make;
	        this.model = model;
	    }
	}
	
	var meriCar = new Vahan("Honda", "Civic");
	
	console.log(meriCar.make); // Output: Honda
    ```

7. **Singleton pattern:**

    Singleton ek aisa object hai jo sirf ek baar instantiate ho sakta hai. Agar aap uske constructor ko baar-baar call karenge toh woh hamesha same instance return karega.

    ```js
    var settings = new (function () {
	    this.theme = "Dark";
	    this.fontSize = "16px";
	})();
	
	console.log(settings.theme); // Output: Dark
    ```