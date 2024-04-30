1. What is printed by line 9? If the code returns an error, explain why.

ANS: `values added:  20`

2. What is printed by line 13? If the code returns an error, explain why.
  
ANS: `final result:  20`

3. What is printed by line 9? If the code returns an error, explain why.

ANS: `values added:  20`

4. What is printed by line 13? If the code returns an error, explain why. 

ANS: ERROR. as we are using the `let` declaration in line 5 `let result = 0;`, the variable result has a block scope and is only accessible by the `if` statement. As the `console.log('final result: ', result)` on line 13 is outside of this, it cannot access it which throws a `ReferenceError: result is not defined`.

5. What is printed by line 9? If the code returns an error, explain why. 

ANS: ERROR. In line 7 we run `result = num1 + num2;` and the result is declared as a constant which means that it cannot be edited/changed. As we are trying to change it, a `TypeError: Assignment to constant variable` error is thrown.

6. What is printed by line 13? If the code returns an error, explain why. 

ANS: ERROR. In line 7 we run `result = num1 + num2;` and the result is declared as a constant which means that it cannot be edited/changed. As we are trying to change it, a `TypeError: Assignment to constant variable` error is thrown.
