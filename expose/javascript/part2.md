1. What will happen at line 12 and why? If the code causes an error, explain why?

ANS: `3` is printed by the console. This is because i has a `var` decelaration which gives the entire function scope to access i. As i is incremented to the lenght of the list `prices`, with the input `[100, 200, 300]` i is incremented 3 times hence 3. Line 12 `console.log(i);` log accesses this and prints `3`. 
