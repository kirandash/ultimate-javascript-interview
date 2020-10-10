# Mod 03 Interview QA

## 03_01 Triple Add
1. tripleAdd(10)(20)(30): returns total of all 3 numbers
    - Sol: For this to work, tripleAdd is a **fn which must return another fn and then another fn**. And the final fn must return the answer.
    - This is called **Currying a fn**: one fn takes multiple arguments and then it will pass the args one by one to a **sequence of fn**, with each fn taking one arg.

## 03_02 What is an IIFE? And Why are they used? Example Code
1. Code out an example IIFE that functions properly
2. Ans: Immediately Invoked Fn Expression.
    * A fn that is executed right after it is created
3. Why IIFE?
    Ans: To preserve a private scope within your function and not spoil/overwrite the global scope viz 3rd party libraries in global scope.
    - Ex: while using jQuery we might accidentally use the $ sign then we won't be able to access jQuery anymore
    - To fix this: It is always a good practice to wrap all our code in IIFE so that we don't overwrite the global variables accidentally.
