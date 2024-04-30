**1. What will happen at line 12 and why? If the code causes an error, explain why?**

ANS: `3` is printed by the console. This is because i has a `var` decelaration which gives the entire function scope to access i. As i is incremented to the length of the list `prices`, with the input `[100, 200, 300]` i is incremented 3 times hence 3. Line 12 `console.log(i);` log accesses this and prints `3`. 

**2. What will happen at line 13 and why? If the code causes an error, explain why?**

ANS: `150` is printed by node.js. line 13 `console.log(discountedPrice)` is trying to print `var discountedPrice = prices[i]*(1-discount);` which has a var scope which is accessible by the entire function. As the last set is the discount of 50% applied to the last entry of `[100, 200, 300]`, 0.5*300=150 which is printed.

**3. What will happen at line 14 and why? If the code causes an error, explain why?**

ANS: `150` is printed by node.js. line 14 `console.log(finalPrice);` is trying to print `finalPrice = Math.round(discountedPrice*100)/100;` which has a var scope defined by `var finalPrice = 0;` which is accessible by the entire function. As the last set is the discount of 50% applied to the last entry of `[100, 200, 300]`, Math.round(150*100)/100 = 150 which is printed.

**4. What will this function return? Give a brief explanation why. If the code causes an error, explain why.**

ANS: it return `[ 50, 100, 150 ]` which is 50% discount applied to `[100, 200, 300]` respectiely. This is `return discounted;` calls for `var discounted
 = []` which has a full function scope and is accessible.
 
**5. What will happen at line 12 and why?  If the code causes an error, explain why (assume this function is being called like the others: discountPrices([100, 200, 300], 0.5))**

ANS: ERROR as `console.log(i);` is calling for `i` which is defined by `let` meaning it has block scope assigned to the for loop in line 6. As line 12 is outside of the for loop, it does not have access and hence  error `ReferenceError: i is not defined` is thrown.

**6.  What will happen at line 13 and why? If the code causes an error, explain why.**

ANS: ERROR as `console.log(discountedPrice);` is calling for `discountedPrice` which is defined by `let` meaning it has block scope assigned to the for loop in line 6. As line 13 is outside of the for loop, it does not have access and hence error `ReferenceError: discountedPrice is not defined` is thrown.

**7. What will happen at line 14 and why? If the code causes an error, explain why.**

ANS: `150` is printed as line 14 `console.log(finalPrice);` is trying to print `finalPrice = Math.round(discountedPrice*100)/100;` which has a let scope defined by `let finalPrice = 0;` which is at the root of the function. let has a block scope but in this instance, the entire function is part of the block so it is accessible. As the last set is the discount of 50% applied to the last entry of `[100, 200, 300]`, Math.round(150*100)/100 = 150 which is printed.


**8. What will this function return? Give a brief explanation. If the code causes an error, explain why.**

ANS: it return `[ 50, 100, 150 ]` which is 50% discount applied to `[100, 200, 300]` respectiely. This is `return discounted;` calls for `let discounted
 = []`  which is at the root of the function. let has a block scope but in this instance, the entire function is part of the block so it is accessible. 

**9. What will happen at line 11 and why? If the code causes an error, explain why.**

ANS: ERROR as `console.log(i);` is calling for `i` which is defined by `const` meaning it has block scope assigned to the for loop in line 6. As line 11 is outside of the for loop, it does not have access and hence  error `ReferenceError: i is not defined` is thrown.

**10. What will happen at line 12 and why? If the code causes an error, explain why.**

ANS: 3 is printed as `length` is defined by `const length = prices.length;` which has block scope. As it is defined in the root of the function, the whole function can access it and as it refers to the length of the input array `prices` which is `[100, 200, 300]`, it prints `3`.

**11. What will this function return? Give a brief explanation. If the code causes an error, explain why.**

ANS: `[ 50, 100, 150 ]`. `discounted` is an array object and the `const` tag does disallow adding new objects. `const discountedPrice = prices[i]*(1-discount);` is repeadtedly redefined which does not violatet that const is immutable. And the discountedPrice when pushed into the list changes its scope. Hence, it return `[ 50, 100, 150 ]` which is 50% discount applied to `[100, 200, 300]` respectiely. This is `return discounted;` calls for `const discounted  = []`  which is at the root of the function. const has a block scope but in this instance, the entire function is part of the block so it is accessible.

**12. Given the above Object, write the notation for:**

A: `student.name`

B: `student["Grad Year"]`

C: `student.greeting()`

D: `student["Favorite Teacher"].name`

E: `student.courseload[0]`

**13. Arithmetic**

A: `32`

B: `1`

C: `3`

D: `3null`

E: `4`

F: `0`

G: `3undefined`

H: `NaN`


