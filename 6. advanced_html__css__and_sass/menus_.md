---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE2MCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.Q2M0H_OxyrzIfu2Y_-do3aSqD9uN0hPt8kHnca6snk4

title: >-
  Menus 
description: >-
  Creating menus using HTML and CSS
---
Menus are a vital part of every website. Here is a guide on how to create them using HTML and CSS. The most common menus are horizontal ones. 

1. Menus are created using unordered lists `<ul>` that are then inverted to become horizontal. 

```html
<ul>
  <li><a href="#">Item 1</a></li>
  <li><a href="#">Item 1</a></li>
  <li><a href="#">Item 1</a></li>
</ul>
```

2. Now that we have the structure of the menu, lets move to the css. First we need to use a display to target the `<li>` of the menu. 
```css
li {
  display: inline; 
}
```

3. Its starting to look like a menu. Now we can make it look prettier by styling the `<a>` tag. 
```css
a {
  text-decoration: none;
  color: white;
  background-color: purple;
  padding: 10px;
}
```

4. It is now a menu, but if we want to add any kind of hover or active state on the links, we would use something called a *pseudo-class*. These are added to selectors but instead of describing a special state, they allow you to style certain parts of a document and are notated by a single `:` in the css. Common ones include `:hover`, `:active`, `:link`, and `:visited`. 

Note: They must go in this order
- `:link` a normal, unvisited link
- `:visited` a link the user has visited
- `:hover` a link when the user mouses over it
- `:active` a link the moment it is clicked


```css
a:hover {
  background-color: teal;
}
```

<iframe height='334' scrolling='no' src='//codepen.io/lexinamer/embed/xEjWjX/?height=334&theme-id=0&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/lexinamer/pen/xEjWjX/'>Basic Menu</a> by Lexi Namer (<a href='http://codepen.io/lexinamer'>@lexinamer</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

