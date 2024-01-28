The difference between Call, Apply and Bind can be explained with below examples,

**Call:** Call() method ek function ko invoke karta hai, jisme diya gaya `this` value aur arguments ek ek karke diye jate hain.

```js
var student = { name: "Rahul", age: 21, course: "Engineering" };

function introduce(greeting1, greeting2) {
  console.log(
    greeting1 + " " + this.name + ", umar " + this.age + " saal, padh rahe hain " + this.course + ". " + greeting2
  );
}

introduce.call(student, "Namaste", "Kaise ho?"); // Namaste Rahul, umar 21 saal, padh rahe hain Engineering. Kaise ho?
```

**Apply:** Apply() function ko invoke karta hai, jisme diya gaya `this` value aur arguments ek array ke roop mein diye ja sakte hain.

```js
var employee = { name: "Priya", designation: "Software Developer" };

function welcome(greeting1, greeting2) {
  console.log(
    greeting1 + " " + this.name + " + this.designation + ". " + greeting2
  );
}

welcome.apply(employee, ["Hello", "Kya chal raha hai?"]); // Hello Priya, Software Developer. Kya chal raha hai?
```

**Bind:** Bind() ek naya function return karta hai, jisme aap koi bhi sankhya ke arguments pass kar sakte hain.

```js
var manager = { name: "Amit", department: "HR" };

function greet(message1, message2) {
  console.log(
    message1 + " " + this.name + ", jo hain " + this.department + ". " + message2
  );
}

var greetManager = greet.bind(manager);
greetManager("Hey", "Kaise ho?"); // Hey Amit, jo hain HR. Kaise ho?
```

Call aur Apply ka upayog lagbhag ek doosre ke badle ho sakta hai. Dono hi turant current function ko execute karte hain. Aapko decide karna hoga ki kya aapko ek array bhejna aasan hai ya phir ek comma separated list of arguments. Aap ise yaad rakh sakte hain ki Call ka istemaal hota hai **comma** (separated list) ke liye aur Apply ka istemaal hota hai **Array** ke liye.

Bind ek naya function banata hai jisme `this` value bind() ke pehle parameter mein set hota hai.