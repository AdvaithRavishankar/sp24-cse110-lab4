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

**14. Comparison**

A: `true`

B: `false`

C: `true`

D: `false`

E: `false`

f: `true`

**15. Explain the difference between the == and === operators**

ANS: `==` performs type conversion so both are the same type and then checks for equality and `===` checks equality without conversion.

**16. Given the above Object, write a for...in loop that will iterate through it and print out the value of the property if the property starts with the letter r, or if the value of that property is an odd number.  (This should be in a JS file part2-question16.js)**

ANS: [https://github.com/AdvaithRavishankar/sp24-cse110-lab4/blob/main/expose/javascript/part2-question16.js](https://github.com/AdvaithRavishankar/sp24-cse110-lab4/blob/main/expose/javascript/part2-question16.js)


**17. If the function above is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result. (This should be in your part2.md). Here we are passing in a function as a parameter, however we can also return a function from another function just as easily, you're encouraged to play around with callbacks as they are used heavily in frontend JS development**

ANS: `[ 2, 4, 6 ]` will be outputs as the function `modifyArray` applies function `doSomething` on each element, adds it to the array. As `[1, 2, 3]` is the input, and `doSomething` multiples each element by 2, `[ 2, 4, 6 ]` is printed.

**18. The above program only prints out the time once when executed. Modify this code such that the program prints out the current time every second.  (This should be a JS file - part2-question18.js) **

ANS: [https://github.com/AdvaithRavishankar/sp24-cse110-lab4/blob/main/expose/javascript/part2-question18.js](https://github.com/AdvaithRavishankar/sp24-cse110-lab4/blob/main/expose/javascript/part2-question18.js)

**19. What is the output of the above code? (This should be in your part2.md)**

ANS:

1

4

3

2
