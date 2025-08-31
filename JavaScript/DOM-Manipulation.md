# DOM Manipulation 

***What is the DOM?***

The DOM is a structure that a browser produces when it reads an HTML file. The document is a Javascript object that represents the HTML file and the browser organizes 
the HTML file as a tree and it's elements as nodes. So if DOM is a sturcture, DOM manipulation is ability to manipulate that structure dinamically using Javascript.

***Why do we need DOM-Manipulation?***

So the main uses of DOM-Manipulation is to add interactivity to our Static HTML file. A normal HTML file is static, which means it does not interact with user. 
But, now using DOM-Manipulation we can make any static page interactive.

***How do we manipulate the DOM?***  
There are many ways and methods to manipulate the DOM, this can be selecting an element in the DOM to change its style, adding or removing an element in the DOM, making elements respond to user inputs and etc...
But here we will focus on the most important ones. 

***1. Selecting Elements:***  
Here before we manipulate any thing first we have to access it, this is also related to DOM-traversal, which means going through or traversing through the DOM.
We select any element by going through the document structure. So there are multiple ways in whcih we can access elements.

  *1.1. document.getElementById('Id)*: this is selecting an element by Id.  
  *1.2. documet.getElementsByClassName('class-name')*: this returns all elements that has given class.  
  *1.3. document.getElementsByTag('Tag')*: retruns elements with the give tag  
  *1.4. document.querrySelector('CSS-selector')*: this method of selecting can select any element that matches the first element of the given css-rule or selector,
                                                which means it is not onfined to one css-rule or selector, we can select any element based on the given css rule.
                                                this only returns the first element that matches this one.  
  *1.5. document.querrySelectorAll('CSS-selector):* This selector returns all elements that matches the css rule that you input.   
  
***2.Chnaging contents and attributes***  
Once we get the elemetns now we should be able to change them, so we can change the text content, attributes, or html elements.  
    *2.1.Changing a content* : We can change the content of an element using this two methods
    
  ```javascript 
  const content = documment.getElementById('heading');
  content.textContent = 'Hello World'; // or We can use 
  content.innerText = 'Hello World';
  ```
  *2.2. Changing/Modifying HTML element* : Here we can modify HTML element using javascript.

  ```javascript
    const heading = document.getElementById('heading');
    heading.innerHTML = "<em> Hello World </em> "; // here we add an html element from JS
```

*2.3. Changing attributes of HTML elements*: Using js now we can change HTML attributes.

 ```javascript
const image = document.querrySelector( '#img');
imgae.setAttribute('src', 'newImage.png');

// setAttribute takes two arrguments one the attribute and the other the new value for that attribute.
```

 
  
                                        
