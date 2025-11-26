# Javascript Storages

There are 4 main different types where we can interact wih storage in javascript, these are   
      1. LocalStorage  
      2. SessionStorage  
      3. Cookies  
      4. IndexedDB   

***1. LocalStorage:***

   This is a storage that is found in the browser that stores informations upto 10mb that can last 
   in the browser as long as you don't delete them. Because of this they are called persistent storages. 

   We use localStortage when we want permanent data storing. 

   There are 3 ways where we can interact with the localStorage in JS  

  *1. Setting an Item:* We use the localStorage.setItem('key', 'value') method to store the data, this will take 2 arguments that are going to be saved as key-value pairs.  
  
  *2. Getting an Item:* We use the localStorage.getItem('key') method to get an item from the storage.  
  
  *3. Remove an Item:*  We use the localStorage.removeItem('key') method to remove an item from the storage.  
  
   ```javascript

// SETTING ITEM(DATA)
localStorage.setItem('name', 'Jhon');

// GETTING ITEM
localStorage.getItem('name');

//REMOVE ITEM
localStorage.removeItem('name');
```

***2. Session Storage:***  

Session storage is a storage type that stores data similar to local storage but temporarily. When ever the user closes the tab the data will be remvoed. 
They work similarly like localStorages, and they have 3 methods

```javascript

//SETTING ITEM
sessionStorage.setItem('username', 'Jhon');

// GETTING ITEM
sessionStorage.getItem('username');

//REMOVE ITEM
sessionStorage.removeItem('username');

```

***3. Cookies***:   

Cookies are a bit different in thier working, we use cookies whenever we want our data to be sent or accessed by the server.
We can also set an expiration time for cookies. Whenever our cookies expire, the browser will delete it and the website 
can nolonger access it. 

We can only access/interact with cookies using the document.cookie object 

```javascript

//SETTING COOKIE
document.cookie = 'name=bob';

//SETTING COOKIE TIME
document.cookie = 'name=bob;' +  new Date new(2050, 0, 1).toUTCstring();

```

***4. IndexDB*** 

This is a Database in the browser we use this type of storage mainly to store larger data upto hundrdes of MBs. Usually for larger apps.

---- 

***source***

1. youtube --- Kyle Web Dev Simplified
2. gpt --- learn/study mode
   








