JavaScript mein do prakar ke equality comparison operators hote hain - strict (=== or !== ) aur type-converting (== or !=). Strict operators type of variable ko dhyan mein rakhte hain, jabki non-strict operators type correction/conversion values ke basis par karte hain.

**Strict Operators Conditions:**

1. **Strings:** Do strings tabhi strictly equal hote hain jab unke characters ka sequence, length, aur corresponding positions mein same hote hain.
2. **Numbers:** Do numbers tabhi strictly equal hote hain jab woh numericaly equal hote hain, yani same number value honi chahiye. Yahan do special cases hain:
    - NaN kisi se bhi equal nahi hota, including NaN khud.
    - Positive aur negative zero ek doosre ke equal hote hain.
3. **Boolean:** Do Boolean operands tabhi strictly equal hote hain jab dono true hote hain ya dono false.
4. **Objects:** Do objects tabhi strictly equal hote hain jab woh same Object ko refer karte hain.
5. **Null aur Undefined:** Null aur Undefined types === ke case mein equal nahi hote, lekin == ke case mein equal hote hain. Matlab, `null===undefined` --> false, lekin `null==undefined` --> true.

**Examples:**
```js
0 == false   // true
0 === false  // false
1 == "1"     // true
1 === "1"    // false
null == undefined // true
null === undefined // false
'0' == false // true
'0' === false // false
[]==[] or []===[] // false, alag objects ko refer karte hain memory mein
{}=={} or {}==={} // false, alag objects ko refer karte hain memory mein
```
