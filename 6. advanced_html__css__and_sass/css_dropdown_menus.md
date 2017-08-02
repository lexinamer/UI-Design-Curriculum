---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4MCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.0GYOs3trjrE3BsA-UC3lwby0qQzqyAIFH5EfGG1aONY

title: >-
  CSS Dropdown Menus
description: >-
  Learning CSS Dropdown Menus
---
# CSS Dropdown Menus

Add a `<ul>` in HTML to form your nav bar. 
``` html
<ul>
  <li><a href="#">About</a></li>
  <li class="dropdown">
    <a href="#">Work</a>
  </li>
  <li><a href="#">Contact</a></li>
</ul>
```

Add the dropdown menu using another `<ul>` and make sure to give both it and the item that will lead to the dropdown descriptive classes
```html
<ul>
  <li><a href="#">About</a></li>
  <li class="dropdown">
    <a href="#">Work</a>
    <ul class="drop-nav">
      <li><a href="#">Design</a></li>
      <li><a href="#">Development</a></li>
      <li><a href="#">Writing</a></li>
    </ul>
  </li>
  <li><a href="#">Contact</a></li>
</ul>
```

Give your global `<ul>` some styling to set it up for the dropdown
```css
ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
```

Now style your global `<li>` and `<a>` to look like you want them
```css
li {
/* EITHER use a float to keep your nav items have no margins */
  float: left;

/* OR give it an inline-block display and add a margin */
  display: inline-block;
  margin-left: 5px;
 }

a {
  background-color: tomato;
  color: white;
  display: block;
  padding: 10px 20px;
  text-decoration: none;
}
```

Dont forget your hover states
```css
a:hover {
  background-color: navy;
}
```

Now we need to style the dropdown list. 

Use positioning on the parent and child elements so that everything stays aligned. We also need to make it default that our dropdown `<ul>` isnt seen

```css
.dropdown {
  position: relative;
}

.drop-nav {
  position: absolute;
  display: none;
}
```

Style the dropdown `<li>` as needed by giving it a width 
```css
.drop-nav li {
  width: 150px;

/* If you gave the `<li>` a margin earlier, you need to reset the dropdown margin so that it stays aligned */
  margin: 0; 
}
```

Now the magic happens to being everything together. So when you hover over the dropdown item, the drop nav will switch display from none to appear.
```css
.dropdown:hover .drop-nav{
  display: block;
}
```

<p data-height="265" data-theme-id="0" data-slug-hash="rLKWrj" data-default-tab="result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/rLKWrj/">Practicing Dropdowns</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
