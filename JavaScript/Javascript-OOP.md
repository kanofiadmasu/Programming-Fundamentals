 # JavaScript Main Concept -- OOP.  

### What is object oriented programming in Javascript?

Like in other programming languages, OOP in javascript is also a prgramming paradigm where we orgnize and structue codes in an object. 

### Objects.
*Object Data type*  

An object in javascript is a bit confusing, becuase in javascript there are javascript object data types and instantiated/class objects. 
JS object data type is a data type, where we store data as a key-value pair, where keys are uniqe and made up of strings and symbols, values can be of any data type.
We can compare this data type with other programming language data types, for example JS objects are similar to python dictionaries, or java's Hashmaps. 
So, generally this object data type is data type that stores data in key-value pair. We can create this objects mainly using the object literal {} or using the **new** key word. 

*Using object literal method*  
   ```javascript
   const Person = {
   name : 'x',
   age: 10,
   isadult: False
   };
   ```
*Using using the new keyword*  
 ```javascript
 const Person = new Object({
 name: 'x',
 age: 10,
 isadult: False
 });
```
*Instance Objects*  

Objects are a collection of properties and methods. Properties are the data the object has and methods are the behaviour of our objcet. 
We can access properties and objcets using the '.' notation or the '[ ]' notation. One thing to notice is In javascript everything is Object including the object data type 
except non-primitive data types. 

The main way where we create objects is throguh constructors, factory functions and in modern JS using the 'class' keyword. Let us define what each way of creating object differ from one
another. 

   1. *Constructors*:
 Constructors are functions that we use to create new objects that has the same shared behaviour and properties.

*Why do we use them?*  
We use constructor functions mainly to create objects that will have the same shared behaviour and properties. Thus, it will help us with code duplication and modularization.

*When do we use them?*  
When we want objects with the same behaviour and properties.  
Before classes, constructors are the way in which  we do Javasript OOP. 

***code***
   ```javascript
   function Car(make, model){ 
   this.make = make,
   this.modle = model

   };

  car1 = new Car('Porsche', 2025);
  car2 = new Car('Mercedes', 2025);
                                    
   ```
 Here Both car1 and car2 have the same properties with different value. Which means we create multiple objects from the same constructor. 

The ***'this' and 'new'*** Keyword 

*this* keyword is like a pointer, it always points to the object that will be created from the constructor function. It is like the 'self' Keyword in python. It will automatically assign the properties and methods of the constructor for every object that will be created based on its blueprint.  

*new* keyword is the main thing that changes ordinary functions into constructors, without the new keyword the function would not be able to create a new object. So thre are four main thing the new keyword does  
  
     1.  Creats an empty object {}
     2.  It will create the constuctor's prototype, which is .prototype the object form which all the
         instances of that constuctor inherit from
     3.  Calls the constuctor with this pointing to the objects that will be created from that object
     4.  Returns the object without expicitly returning it

2. *Factory Functions*:
   This is another way of creating objects, more simpler and straight forward, we don't need to use the 'new' and 'this' keyword to an object. Factory functions creats and retruns an object.
   Return statment is explicitly written inside the fucntion.

   They may be usefull, for beginners as they are straight forward and simple. And other main thing is factories are good for hiding private varaible or achiving encapsulation, because of javascript closures.

   ```javascript
      function Person(name, age){
      return {
      name : name,
      age : age,
      }
      };
   
      person1 = Person('x', 10);
      person2 = Person('y', 20);
   
      // Here we can see that the function doesn't have any new or this keyword.
      ```

3. *Class*

this is a new method to creat an object, where we use the *class* keyword to create objects with the same property and method. This way of creating objects is the same with constructor functions excpet that in this way we use class instead of functions. 

The main pourpose using class is the  simpler syntaxes, and access to achive encapsulation through (#) this special symbol. Otherwise, classes do exactly the same thing as constructors behind the scene.

   ```javascript
   class Person {
   constructor(name, age){
      this.name = name,
      this.age = age,
   }
   fullName() {
   return `Hello m name is ${this.name} and I am ${this.age} years old`;
   }

const person1 = new Person('x', 40);
const person2 = new Person('y', 50);
   };
   ```
So these are the 3 ways in which we can create objects.  


 
 
 



 


 
 
