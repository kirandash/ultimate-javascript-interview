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

## 03_05 this keyword
1. What is the this keyword and how is it used?
2. Ans:
    * this refers to whatever object it is directly inside of. Ex: in global env: this referes to global window object

## 03_06 Hoisting - var, fn expression, fn declaration, in - global and fn scope
1. What variable and fn hoisting is and how it works?
2. Ans: 
    * **Definition**: In JS variables and fns are hoisted to the top of the scope that they are declared in.
        - scopes are either global scope of function scope
        - Variable and fn hoisting is basically a process in which JS interpreter looks through the code to find out all the var and fn declarations and it hoists those declarations to the top of the file. but not the assignments. Just the declarations.
    * For variables, fn expressions: declarations are hoisted to the top
    * For fn declarations: hoisting is different.: the whole fn with it's definition or assignment is moved to the top of the file.
    * Also if we are declaring var and fn inside a parent fn, the hoisting of those only happens in the parent fn.

## 03_06 Hoisting - var vs let and const
1. The var and fn hoisting to top of the global or fn scope is true only when we use the var keyword which is fn scoped.
    - global scope
    - function scope
2. But if we use the let or const kekywords (block scoped), we have one more scope to think of
    - global scope
    - function scope
    - block scope (for loop, if else, while etc.) For let and const: the variables will be hoisted to top of block scope.
3. **Important**: 
    - Although var is initialized with undefined on hoisting, let and const can not be accessed before it is defined or assigned any value.

## 03_07 scope and self
1. method on an obj will have this pointing to the obj
2. method inside method will loose it's scope from obj and point to the global scope.
    - To fix: use **self or declare this in global scope**

## 03_08 == vs === comparision operators
Ans: 
* == (equals)
    - tests for abstract equality
    - doesn't test for data type
* === (strict equals)
    - tests for strict equality
    - tests for data type
* Under the hood
    - comparing number and string: 
        - string is converted to a number
        - comparison is made
    - comparing boolean and non-boolean
        - non boolean converted into boolean
        - comparison is made
    - Comparing obj and primitive data type
        - obj is converted to primitive data-type
        - comparison is made

## 03_09 Log Number Function - re declaring a variable - hoisting
1. Redeclaring variable will re hoist it
2. JS first checks in immediate scope and then the outer scope
3. var is an ES5 JS feature - old code

## 03_10 use strict
1. What does strict mode do to your code?
2. What are the benefits of using strict mode?
3. Ans:
    * 'use strict'
        - main purpose: Enforce **stricter parsing and error handling** in your code
4. Features
    - prevents the use of global variable ex: variable declaration without var, let, const
        - prevents Duplicate parameter name
        - prevents deletion of non deletable items
5. Benefits:
    - helps during the development process for easy error detection
    - helps fail fast and fail loudly
    - so we can detect error sooner

## 03_11 Curry Function
1. Curry given fn
2. single fn with multiple args ---> multiple sequence of fn with each fn limited to one or part of arg
3. Add a real time application example
    - when one of the arg is of fixed value viz: calculating time taken to cover a fixed distance for different speeds

## 03_12 Counter Function - fn to keep track of itself with closure
1. Write a fn that keeps track of how many times it was called and return that number
2. all functionalities should be inside the fn. non outside
3. The best way for a fn to keep track of itself is using a **closure**

## 03_13 Logging X and Y
1. var x = y = 200; ---> translates to var x; y; y = 200; x = y; y will be created as global var since no let, var, const is supplied.
2. To avoid such issues: better to use 'use strict'

## 03_14 call and apply methods
1. Describe javascript .call() and .apply() methods
2. How do they function?
3. What arguments do they take?
4. How are they different?
5. call method:
    - call method is a **native JS method on the function prototype object**
    - any fn defined in JS will be able to use the call()
    - call method gives us an alternative way of calling fn instead of the traditional way
    - gives us a **different way to pass arguments**
    - gives us a way to **change context of this** keyword as well which normal fn does not give.
6. syntax: `call(this context, args)`

## 03_14 apply method
1. apply method is similar to call method but the difference is how the arguments are sent. **AS AN ARRAY**

## 03_15 Determine list2
1. **passing data by reference vs passing data by value**
    - primitive data types are always passed by value viz: string or number
    - non-primitive data types are passed by reference viz: arrays objects
2. Once array is reassigned, new array will still point to the old array
    - changing the individual value of list1 won't affect list2 bcoz underlying object or reference is still the same

## 03_15 Copying Array data - without reference - slice, concat, spread operator
* Using array Methods:
1. list2 = list1.slice()
2. list2 = list1.concat([])
* use spread operator
* use empty array and loop in through for loop
