# Functions 

In JS or anyother programming laguages Functions are a piece of code/program that excutes a certain task. 
Functions have the following things. 
1. Parameter : This are the input name that we pass to a function during function declaration.
2. Arguments : Are the exact inputs values that we pass them during function calling.
 
In JS there are multiple types of functions these are,

    1. Function Decalaration/Normal function
    2. Arrow fucntions
    3. Self Invoking/Immideatly Invoked functions
    4. Higher order functions
    5. Constructor functions
    6. Factory functions
    7. Generator functions
   
   ---
1. Function declaration is a normal function that has name and can be called.
     ```javascript
     function name(para1, para2) { // fucntion declaration and passing parameter 
     sum = para1 + para2; // computation
     console.log(sum);  
     };
     name(2, 3);  // 2 and 3 are arguments, name() is function calling
    ```
2. Arrow function is a shorthand function that is introduced in ES6, where we use an arrow sign to create a function

   ```javascript
   const name = (para1, para2) => { // here we use the arrow sign instead of function and the parameters are stored inside parantherssi 
   const sum = para1 + para2; // computation 
   console.log(sum);
   }
   name(2, 3) // this is calling the function to excute. 
   ```
3. Self Invoking / immediately invoked function  
   This are functions that we don't need to call for execution, rather they are excuted immediately after they are defined, this is achieved by palcing them inside a paranthesis.
   ```javascript
   (function name(para1, para2) {
   sum = para1 + para2;
   console.log(sum);
   }); // here you can see that we placed the whole function expression inside a paranthesis, which means it will excuted immediately after being declared. 
   ```

4. Higher order functions : this are functions that either take other functions as an argument or returns them as an argument. It has to do one or both. 

 HOF are present in javascript, because JS treats functions as first class citizens, which means functions can be treated as other date types, 
 they can be assgined to a variable and also returned as a result.   
 
   4.1. Callbacks: these are functions that take other functions as an argument.  
   
   for example: 
   ```javascript
  function greet(name, callback) {
  console.log('Hello' + name);
  callback();
  };
  greet('x',  () => ('Wellcome'));
  // so here greet is a callback function because it takes the callback function as an argument.
  ```
  4.2. array higher order functions(methods) map/filter/reduce
     4.2.1. map: is a HOF that applies a function to every element of  array. It takes a callback function as an arrgument and returns an array. 

   ```javascript 
   function mulitply(n) { 
   return  n * n;
   };
   arr = [1, 2, 3, 4]
   console.log(arr.map(multiply)); // this takes a function

   };

   ``` 
   4.2.2. Filter: this method as the name it will filter elements and return elements that satisfy the condition. 
   
  ```javascript

 
      function multiply(n) {
        return n % 2 === 0;
      }
      
      arr = [1, 5, 3, 4];
      evens = arr.filter(multiply);
      console.log(evens);
// here the out put is going to be [4] because it is the only element that satisfies the condition.
 ```
  4.2.3. Reducue: this also as the name suggests it will reduce the reduces the elements by combining them into one element.


Constructors and Factory fucntions are Explained in the OOP section. 




















   




   

