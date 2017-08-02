---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE5MCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.uPLHF7urER-5YAEC4BnHwtn8z83iogfwkp8C2T4um7Q

title: >-
  Understanding the DOM
description: >-
  A quick tour of the Document Object Model and its role in the browser
---
# What is the DOM?
When a web page has loaded in the browser, you have access to the elements via the DOM. We model the nested structure of an HTML page with the DOM (Document Object Model) Tree. The browser makes a "map" of all the elements on a page.

![understand-dom.png](https://tiy-learn-content.s3.amazonaws.com/8565897f-understand-dom.png)

# Understanding the DOM
In short, the **Document Object Model** (DOM for short) is a can be thought of as a set of functionality wrapped around the HTML and CSS in a web page. 

A helpful analogy is an apartment building. To change paint colors, add or remove walls, rewire electrical work, and so on, tenants go through a _landlord_ who approves and allows changes in an organized way. Rather than just taking a sledgehammer to load-bearing wall, tenants request the change, and the request is approved or denied. The landlord can also provide information about the current state of things, like when repairs or scheduled. 

In this case the apartment is your live HTML and CSS in a browser, you're the tenant, and the DOM is the landlord. In other words, the DOM is the interface between you and the changes you'd like to make.


# Javascript Methods
Your browser automatically builds a Document Object to store the DOM of a page. We can use Javascript to manipulate the DOM or our HTML/CSS code.  

To change a page:
1. Find the DOM node and store it in a variable
2. Use methods to manipulate the node


### By ID
You can find a single node by id using the method:
<br>`document.getElementById('id');`


### By Class Name
You can find a single node by class using the method:
`document.getElementByClassName('class');`


### By Tag Name
You can find certain types of HTML elements (multiple nodes) using this method:
`document.getElementsByTagName('tagName');`
	
		  
### By Query Selector
You can find a collection of more specific HTML elements using this method:
`document.querySelector('query selector // for example div');`

What gets returned by querySelector is the first element it finds - even if other elements exist that could get targeted by the selector.

`document.querySelectorAll('query selector // for example #parent .child');`

What gets returned by querySelectorAll is a list of the elements that match the specified group of selectors.



# Javascript Properties  
Properties are the values associated with a JavaScript object. So far, we have been using them with objects, arrays, and dot notation.

```js 
var object = {
   property1 : value,
   property2 : value2,
   property3 : value3
}

// to be called using the following

object.property1;
```

Javascript has a lot of useful built in properties that can help us do things in the DOM such as store values, print to the HTML page, and change styles. Here are some of the most common:



### Storing a value 
You can store the value of an element by using the value property. 

`<input id="text-input">`

`document.getElementById("text-input").value;`



### Storing the numerical value
By default, Javascript stores values as a string. You can store the numerical value by using the parseInt property to parse out the value as an integer. This would be necessary in an addition calculator.

`<input id="number-input">`

`parseInt(document.getElementById("number-input").value);`



### Setting and removing Attributes 
You can set and remove attributes to certain elements depending on the action or condition. 
`<h1>This is a boring generic h1 tag</h1>`

- You can add a class attribute called red: 
`document.querySelector("h1").setAttribute("class", "red");`

- You can remove a class attribute called red: 
`document.querySelector("h1").removeAttribute("class", "red");`



### Styling an element
You can change page and element styles through the style property. 

`<h1 id="change-me">Change Me</h1>`

- To change one styling property: 
`document.getElementById("change-me").style.backgroundColor = "green";`

- To Change multiple styling properties: 
`document.getElementById("change-me").setAttribute("style", "background-color: green; color: orange;");`



### Printing to the HTML page
You can print something to the html page using the inner html property

`<div></div>` (this is an empty div)


`document.querySelector("div").innerHTML = "Print this text to the page";`



# Javascript Events
An 'event' is a type of object that is created when the user interacts with a web page. For example: onClick, do something.

There are a [ton](https://developer.mozilla.org/en-US/docs/Web/Events) of events in javascript Some of the most common:
- click
- mouseover
- open
- load
- submit


# Javascript Event Listeners
An event listener is a function that listens for an event. When that event is emitted, the function will be called automatically. 

There are several ways you can use event listeners to talk between HTML and Javascript. 

For example, lets say we want to find the date on the click of a button:
`<button id="click-me">Click Me For Date</button>`


### addEventListener()
The add event listener method attaches an event handler to the specified element. 

Here is the syntax: 
`element.addEventListener(event, function, useCapture);`

`document.getElementById("click-me").addEventListener("click", displayDate);`



### .onEvent method
The on event method binds a function to an element that occurs on an event.


Here is the syntax: 
`element.onclick = function() {do something};` 


`document.getElementById("click-me").onclick = function() {displayDate};`
 


### .onEvent method in HTML
As a shortcut, you can call a function directly from your HTML:

`<button onclick="clickMe()">Click Me for Date</button>`


`function clickMe() {displayDate};`
 


# In Class Problems
- Custom Login Message
- Simple Addition Calculator 
- Color Changer
- Mad Lib with input forms


# Peer Programming: Bill Calculator
1. Create a tip calculator that takes the total bill and lets you select either 15%, 20%, or 25% tip. Output the final total after tip. 
2. Now see if you can take the new total and split the bill (after tip) 2, 3, or 4 ways. 
3. Give it some styling.  

# Peer Programming: User Profile
1. Take some profile information about a user (name, email, username, etc) using inputs
2. Output that information back onto the page in a readable, hierarchical way. 
3. Give it some styling.




