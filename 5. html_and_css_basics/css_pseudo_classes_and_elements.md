---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4MSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.yD5pPGhc_4drDqZIfjP2UnPtn9k5K1uGE_31k91p9Vc

title: >-
  CSS Pseudo Classes and Elements
description: >-
  A look at special CSS psuedo classes and elements
---
# Pseudo Classes
A pseudo-class is a phantom state or specific characteristic of an element that can be targeted with CSS.

They are always preceded by a colon `:`

## Common Pseudo Classes
`:link` - This represents the “normal” state of links and is used to select links that have not yet been visited.

`:visited` - Selects links that have already been visited by the current browser.

`:hover` - When the mouse rolls over the element, it shows the hover state. It doesn’t have to be restricted to links, although that is the most common use case.

`:active` - Selects the element that has been “activated” either by a pointing device or by a tap on a touchscreen device. It occurs between the mouse button being clicked and being released.

`:focus` - Represents the state when the element is currently selected to receive input from input devices (keyboard). For example, if a user uses Tab on a button, it enters its `:focus` state but is a user clicks with a mouse, it enters the `:active` state.

## Position Based Pseudo Classes
![number](https://css-tricks.com/wp-content/csstricks-uploads/relationalpseudos2.png)


# Pseudo Elements
Pseudo-elements are like virtual elements that we can treat as regular HTML elements. They don’t exist in the document tree or DOM. This means we don’t actually type the pseudo-elements, but rather create them with CSS.

In CSS3, the double colon `::` was introduced for pseudo elements to distinguish between them and the pseudo classes. 



## Before and After
`::before` and its sibling ::after` are pseudo elements which allows you to insert content onto a page from CSS without it needing to be in the HTML. While the end result is not actually in the DOM, it appears on the page as if it is, and would essentially be like this:

```
div::before {
  content: "hi";
}
```

will render like this in the html 

```
<div>
  hi
  <!-- Rest of stuff inside the div -->
</div>
```

### What You Can Input
- `content: "text";` Inserts a string of text and numbers 
- `content: url(/path/to/image.jpg);` The image is inserted at it's exact dimensions and cannot be resized. Since things like gradients are actually images, a pseudo element can be a gradient.
- `content: "";` - Useful for clearfix as seen below

```css
.clearfix::after {
    content:"";
    display:block;
    clear:both;
}
```

<p data-height="399" data-theme-id="0" data-slug-hash="dvoxMQ" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" data-pen-title="Clearfix Pseudo Elements" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/dvoxMQ/">Clearfix Pseudo Elements</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


## Other Pseudo Elements
`::first-letter` Selects the first letter in a line of text. Would allow you to enhance typographic appeal of a paragraph.

`::first-line` Targets the first line of an element. It works only on block-level elements, not inline elements.

`::selection` Styles the portion of a document that has been highlighted.


## References
- https://www.smashingmagazine.com/2016/05/an-ultimate-guide-to-css-pseudo-classes-and-pseudo-elements/

