---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE5MSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.SDH4PPuNoyl7P_ee_aHDtWsUuNafCfkOK8B_N_pbMJs

title: >-
  Introduction to jQuery
description: >-
  Now that we know the fundamentals of JavaScript, we are going to learn the basics of the jQuery library.
---
# What is jQuery
With a basic understanding of JavaScript and some of it’s foundations, it is time to take a look at jQuery. jQuery is an open source JavaScript library that simplifies the interaction between HTML, CSS, and JavaScript. 

Another way to think of jQuery is that it is the Sass of Javascript. 

### Getting Started
The first step to using jQuery is to reference it from within a HTML document. As previously mentioned with JavaScript, this is done using the script element just before the closing `</body>` tag. Since jQuery is it’s own library it is best to keep it separate from all the other JavaScript being written.

When referencing jQuery there are a few options, specifically as whether to use the minified or uncompressed version, and as whether to use a content delivery network, CDN, such as [Google hosted libraries](https://developers.google.com/speed/libraries/).

```
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
<script src="script.js"></script>
``` 

### jQuery Object
jQuery comes with it’s own object, the dollar sign, $, also known as jQuery. The $ object is specifically made for selecting an element and then returning that element node to perform an action on it. 
```
$();
jQuery();
```

### Document Ready
Before trigging any jQuery to traverse and manipulate a page it is best to wait until the DOM is finished loading. Fortunately jQuery has a ready event, .ready(), which can be called when the HTML document is ready to be altered. By placing all of our other custom written jQuery inside of this function we can guarantee that it will not be executed until the page has loaded and the DOM is ready.
```
$(document).ready(function(){ 
  // jQuery code 
});
```

# Selectors
jQuery has done a great job of making the task of selecting an element, or elements, extremely easy by mimicking that of CSS. 

Invoking the jQuery object, $(), containing a selector will return that DOM node to manipulate it. The selector falls within the parentheses, ('...'), and may select elements just like that of CSS.

- $('.feature');           // Class selector
- $('#feature');           // ID selector
- $('ul li a');            // Descendant selector
- $('em, i');              // Multiple selector
- $('p:hover');            // Pseudo-class selector

# Manipulation
Using jQuery, you can manipulate these elements by either adding or changing attributes or styles. Additionally, elements may be altered in the DOM, changing their placement, removing them, adding new elements, and so forth.

### Getting & Setting
The manipulation methods to follow are most commonly used in one of two directives, that being getting or setting information. Getting information revolves around using a selector in addition with a method to determine what piece of information is to be retrieved. Additionally, the same selector and method may also be used to set a piece of information.
```
// Gets the value of the alt attribute
$('img').attr('alt');

// Sets the value of the alt attribute
$('img').attr('alt', 'Wild kangaroo');
```

### Attribute Manipulation
Attributes within elements can be modified. A few options include the ability to add, remove, or change an attribute or its value.
```
$('li:even').addClass('even-item');
$('p').removeClass();
$('abbr').attr('title', 'Hello World');
```

Know that you can also manipulate the styling using jQuery. Here is a great resource to learn more: http://learn.shayhowe.com/advanced-html-css/jquery/

<br>
# jQuery Methods
You can use the dot notation just like we learned in Javascript to use a variety of built in jQuery methods. The possibilities are endless and it helps us start to build UI Elements. 

Use the awesome [jQuery Library](https://api.jquery.com/) to see them all, including examples and how to use. 

`.click()`
Bind an event handler to the element that triggers on click


`.addClass()`
Adds the specified class(es) to each element in the set of matched elements.

`.removeClass()`
Revmoes the specified class(es) to each element in the set of matched elements.

`.slideToggle()`
Display or hide the matched elements with a sliding motion.

`.mouseover()`
Bind an event handler to the “mouseover” JavaScript event, or trigger that event on an element.

`.scrollTop()`
Get the current vertical position of the scroll bar for the first element in the set of matched elements or set the vertical position of the scroll bar for every matched element.


# jQuery Plugins
For a designer, plugins are one of the most powerful aspects of jQuery. A jQuery plugin is simply a new method that we use to extend jQuery's functionality. Pretty much any kind of UI behavior that you can think of, has probably been already created using a plugin. 

The good ones will be well documented with examples, demos, and usage instructions. You might have to weed through a few of the bad ones to get to a good one. 

- [jQuery Plugin Registry](http://plugins.jquery.com/)
- Google and Codepen is a great resource for finding plugins. 


# Practicing jQuery
Hide and Show
<p data-height="235" data-theme-id="0" data-slug-hash="xOaNWA" data-default-tab="js,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/xOaNWA/">Hide/Show</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Toggle On and Off
<p data-height="276" data-theme-id="0" data-slug-hash="NALVYk" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/NALVYk/">Slide Toggle</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

### Fading Colors
1. Create 2 boxes in html and give them some styling. 
2. Using the slideToggle() method, make them appear and disappear when you click a button.
3. Make them hidden by default
3. Change the speed 

### Popup Window
1. Create 3 `<divs>` that talk about your favorite tv shows and create buttons that will link to them
4. Use [Remodal](http://vodkabears.github.io/remodal/#) to make the `<divs>` appear in a popup when you click on the button.

### Hamburger Menu
1. In pairs create a normal menu and a mobile menu 
2. Give them basic styling in css FIRST 
2. Use a media query and jQuery to have the mobile menu toggle when it gets to mobile size. 
(hint. heres how your might get the hamburger icon: `<a id="nav-toggle" href="#">&#9776;</a>`)

