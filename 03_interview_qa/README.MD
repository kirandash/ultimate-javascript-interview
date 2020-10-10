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

## 03_03 Button - onClick in for loop - sol: iife, fn, let
1. Online code editor for HTML, CSS, JS: jsbin.com
2. What will be alerted on clicking each button
3. Ans: 6 for all buttons
4. **Fix**: 
    * **Using IIFE** to preserve value of i in it's own scope for onClick events
    * Using separate fn scope and passing button, i
    * Using **let** keyword for i variable (ES6 solution) - let has a block scope compared to var scope which has a global scope

## 03_04 Closures
1. What is a closure? Code out an example closure
2. Ans: 
    * A closure is an inner function that has access to the scope of an enclosing function
    * A closure has access to **variables** in 3 separate scopes:
        - variables in it's own scope
        - variables in scope of the outer fn
        - variables in the global scope
    * The closure also has access to
        - it's own parameters
        - parameters of outer fn
