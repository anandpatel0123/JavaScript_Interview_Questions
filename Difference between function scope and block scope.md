***what is the scope of a variable?***
Scope kisi variable ya function bhi ho sakta hai but logic same rehta hai. To jab hum bolte hai scope uska matlab, usiki lifetime or availability se hota hai.
Jiase agar tum ek variable ek function ke andar declare karte ho to vo variable sirf usi function mai accessible hota hai, other fucntions mai nahi.

```js
function a(){
    let x = 10;
} 

function b(){
    console.log(x);
}
a();
b();
// while running we get error
`console.log(x);
             ^
ReferenceError: x is not defined`
```

To jab hum `x` ko function `b()` mai access karne ki kosis karte hai to error aati hai, qki uska scope ya availability sirf function `a()` mai hai.
To ye variable `x` local hai function `a()` mai.

***Note:*** variable ka scope `Local` or `Global` ho sakta hai. (Jaise abhi ye Local hai)

***Global Scope :*** Jab hum variable ko sabhi function ke bahar declare ya define karte hai to uska scope `Global` ho jata hai and wo sabhi functions mai accessible hota hai.

```js
let x = 10;
function a(){
    x=x+5;
}
function b(){
    console.log(x);
}
a();
b();
```

***Function Scope vs Block Scope***
ES5 has function scope because of `Hoisting`.
ES6 does not have `hoisting` , it has block scope.

***Note:*** Agar aap `var` keyword se variable decalre karte hai to `hoisting`
hoga.

***Hoisting*** : jab aap variable declare karte ho `var` keyword ki help se to compiler sare declaration top mai shift kar deta hai use hoisting kehte hia. 
Example: 
```js
// Normal code:
console.log(x); //Output: undefined
var x = 10; 
// humne x pehle access kiya and define baad mai. To Internally compiler sabhi variable ko jo *var* se decalre kiye hi unko top mai shift kar deta hai

// Compiler code (behind the scene) Upper wale code ko compiler is tarah se interperate karega
var x;
console.log(x); //Output: undefined
x = 10; 
```

So, hum `hoisting` ko hi `function scope` bolte hai. Jaha par aap var keyword ka use karte hai, aap ek function mai same variable declare nahi kar sakte. 

```js
function a(){
    var x = 10
    if(x) {
        var x = 50;
    }
    console.log(x); //Output: 50
}
a(); 
// top aap dekho print hona chahiye tha 10 but hua 50, because hoisting ki wajah se x ka scope poore function mai hai.

// Yahi hum let se karte hai, to uska scope block mai ho jata hai
function a(){
    let x = 10
    if(x) {
        let x = 50;
    }
    console.log(x); // Output 10
}
a();
```

