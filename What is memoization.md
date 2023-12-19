Memoization ek functional programming technique hai jo ek function ki performance ko badhane ki koshish karta hai, uske pehle se calculate kiye gaye results ko cache mein store karke. Har baar jab memoized function ko call kiya jata hai, uske parameters ka use cache mein index banane ke liye hota hai. Agar data cache mein maujood hai, toh function ko pura execute kiye bina hi woh data return kiya ja sakta hai. Varna function ko execute kiya jata hai, aur fir result ko cache mein add kiya jata hai. Chaliye ek addition function ke example se samajhte hain, jisme hum memoization ka use karenge.

**Memoization Ka Example:**

```js
	const memoizAddition = () => {
	  let cache = {};
	  return (value) => {
	    if (value in cache) {
	      console.log("Cache se fetch kiya gaya");
	      return cache[value]; // Yahan, cache.value ka use nahi kiya ja sakta, kyunki property name number se shuru hota hai, jo JavaScript mein valid identifier nahi hai. Isliye, isko square bracket notation se hi access kiya ja sakta hai.
	    } else {
	      console.log("Result calculate kiya gaya");
	      let result = value + 20;
	      cache[value] = result;
	      return result;
	    }
	  };
	};
	
	// memoizAddition se return kiya gaya function
	const addition = memoizAddition();
	
	console.log(addition(20)); //output: 40 calculate kiya gaya
	console.log(addition(20)); //output: 40 cache se fetch kiya gaya
```

Yahan, humne ek `memoizAddition` function banaya hai, jisme ek cache object hai. Fir humne ek function return kiya hai, jise hum `addition` variable mein store kar rahe hain. Jab hum `addition(20)` ko do baar call karte hain, toh pehli baar woh calculate hota hai aur result 40 hai. Dusri baar jab hum wahi value pass karte hain, toh cache se hi woh result fetch ho jata hai aur fir se execute nahi hota. Is tarah se memoization ka use karke hum performance improve kar sakte hain.