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

  *1.1. document.getElementById("Id")*: this is selecting an element by Id.
  
  *1.2. documet.getElementsByClassName("class-name")*: this returns all elements that has given class.  
  
  *1.3. document.getElementsByTag("Tag")*: retruns elements with the give tag  
  
  *1.4. document.querySelector("CSS-selector")*: this method of selecting can select any element that matches the first element of the given css-rule or selector,
                                                 which means it is not confined to one css-rule or selector, we can select any element based on the given css rule.
                                                 this only returns the first element that matches this one.  
  
  *1.5. document.querySelectorAll("CSS-selector"):* This selector returns all elements that matches the css rule that you input.   
  
***2.Chnaging contents and attributes*** 

Once we get the elemetns now we should be able to change them, so we can change the text content, attributes, or html elements.  
    *2.1.Changing a content* : We can change the content of an element using this two methods
    
  ```javascript 
  const content = documment.getElementById('heading');
  content.textContent = 'Hello World'; // or We can use 
  content.innerText = 'Hello World';
  ```
Here there is a few difference between 'textContent' and 'innerText'. innerText returns or displays element as the user would see it and it respects styles applied. 
While 'textContent' returns text directly from the HTML, and it ignores the style applied to it.  

```html
<div id="example">
  Hello
  <span style="display: none;">Hidden</span>
  <span>World</span>
</div>
```
```javascript
const div = document.getElementById('example');

console.log(div.textContent);  // "Hello Hidden World" (includes hidden text)
console.log(div.innerText);    // "Hello World" (excludes hidden text)
```
 
  *2.2. Changing/Modifying HTML element* : Here we can modify HTML element using javascript.

  ```javascript
    const heading = document.getElementById('heading');
    heading.innerHTML = "<em> Hello World </em> "; // here we add an html element from JS
```

*2.3. Changing attributes of HTML elements*: Using js now we can change HTML attributes.

 ```javascript
const image = document.querySelector( '#img');
imgae.setAttribute('src', 'newImage.png');

// setAttribute takes two arrguments one the attribute and the other the new value for that attribute.
```

*2.4. Adding/Removing Classes of an element*: We can add, remove, and change a class in an element using JS. 

 ```javascript
 const element = document.querySelector('.text-1');
 element.classList.add('greeting'); // This adds the class greeting to the element
 element.classList.remove('text-1'); // This removes the class greeting from the element
 element.classList.toggle('greeting');// This will add the class greeting if it doesn't exist before, and will delete it if it does exist.
 ```
***3. Changing the style of and element***  

Using DOM we can also manipulate the style of an element. We are able to do this through the *.style* objcet. 

```javascript
const element = document.querySelector('.text-1');
element.style.color = 'red';
element.styel.fontSize = '24px'; // Here as we can see we changed the style element.
``` 

***4. Creating, Adding and removing elements***  

We can also create, add, and remove elements using DOM. 

*4.1. Creating Element*: We use '.createElement' to create an element.

```javascript
const newElement = document.createElement('li');
newElement.textContent = 'Hello';
```
*4.2 Appending element*: Once we created an element we should always add it or append it. If we don't append it we wouldn't see it. 

There are two ways to append an element. The first one is .append and the other one is .append child 

*.appendChild*: this one append elements to the DOM but it only accepts one element at a time, it retruns the element that it append, it only accepts node elements-- doesn't accept strings other non-node elements, and less flexible.  

*.append*: this one accepts multiple inputs or can append multiple elements, we can append non-node elements, and it is more flexible. 

```javascript
const newElement = document.createElement('li')
newElement.textContent = 'Hello';

document.append(newElement); // or we can do
document.appendChild(newElement);
```

*4.3. Removing an element*: 

```javascript
const element = document.querySelector('.text-1');

element.remove(); // it is simple to remove elements
```

***5. EventListeners*** 

We use event listeners when we want to respond to user events on the page, events like scroll, hover, click, input, submit, etc... 

event listners has two arguments, the first one is the event that trigger the output, and the second is a callback fucntion which will do the task. 

```javascript
let btn = document.querySelector("#myBtn");

btn.addEventListener("click", function() {
  alert("Button was clicked!");
});
// here the event is "click" and alert is the response to that event.
```

So the above DOM Methods are the core DOM manipulation methods we will use, the above methods cover 80% of the DOM methods we will need. 

---

*Sources* 
1. Youtube: WebDevSimplified, BroCode
2. GPT: study/learn mode
  
                                        



