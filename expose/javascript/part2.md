** 1. What will happen at line 12 and why? If the code causes an error, explain why? **

ANS: `3` is printed by the console. This is because i has a `var` decelaration which gives the entire function scope to access i. As i is incremented to the lenght of the list `prices`, with the input `[100, 200, 300]` i is incremented 3 times hence 3. Line 12 `console.log(i);` log accesses this and prints `3`. 

** 2. What will happen at line 13 and why? If the code causes an error, explain why? **

ANS: `150` is printed by node.js. line 13 `console.log(discountedPrice)` is trying to print `var discountedPrice = prices[i]*(1-discount);` which has a var scope which is accessible by the entire function. As the last set is the discount of 50% applied to the last entry of `[100, 200, 300]`, 0.5*300=150 which is printed.
