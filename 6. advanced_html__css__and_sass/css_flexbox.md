---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE3OSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.-ON9OIQqOdiVctcqqUHLFDqMB9LOxK8SFX84glv59Bc

title: >-
  CSS Flexbox
description: >-
  Learn flexible layout with Flexbox
---
## What is Flexbox
Flexbox is a newish part of CSS. Flexbox tries to help fix the inadequacies of older methods of CSS positioning. As we've seen, positioning in CSS can be tricky. Flexbox attempts to solve this by offering a more flexible yet robust positioning model. 

Flexbox should not be used for main page layout and instead for UI elements. It is helpful for laying out items in a single dimension – in a row OR a column. Grid is for layout of items in two dimensions – rows AND columns.

## How it Works
Flexbox layout, or flexbox, distributes space along a single column or row. It does so like float layouts, but better! While flexbox is now supported by many browsers but not all. 

![flexbox cheat sheet](http://spaceninja.com/content/images/2015/07/flex-intro.svg)
<br>

A Flexbox layout consists of a `flex container` that holds `flex items`. The flex container can be laid out horizontally or vertically. This is referred to as the `main axis`. The other container is known as the `cross axis. 

![flexbox cheat sheet](http://spaceninja.com/content/images/2015/07/axis-both.svg)
<br>

## Common Properties
To get started, all you need is to add a `display` property to your parent container. This defines your flexbox and enables flex content for all of the children.

```css
.flex-container {
   display: flex; 
}
``` 

You can then use the following properties to create your layouts.

### On the Container

`flex-direction: row | row-reverse | column | column-reverse;`
<br>
This establishes the main-axis, thus defining the direction flex items are placed in the flex container

`justify-content: flex-start | flex-end | center | space-between | space-around;`
<br>
This defines the alignment of how flex items are laid out along the main axis. 

`align-items: flex-start | flex-end | center | baseline | stretch;`
<br>
This defines the default behavior for how flex items are laid out along the cross axis.

`flex-wrap: nowrap | wrap | wrap-reverse;`
<br>
By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.

`align-content: flex-start | flex-end | center | space-between | space-around | stretch;`
<br>
This aligns a flex container's lines in the cross-axis only when there is more than one row of flex items.


### On the Child Elements (Flex Items)
`order: <integer>;`
<br>
By default, flex items are laid out in the source order. However, the order property controls the order in which they appear in the flex container.

`flex-grow: <number>; /* default 0 */`
<br>
This defines the ability for a flex item to grow if necessary. It dictates what amount of the available space inside the flex container the item should take up.

`flex-shrink: <number>; /* default 1 */`
<br>
This defines the ability for a flex item to shrink if necessary. Negative numbers are invalid.

`flex-basis: <length>;`
This defines the default size of an element before the remaining space is distributed. It can be a length (e.g. 20%, 5rem, etc.) or a keyword.

`align-self: auto | flex-start | flex-end | center | baseline | stretch;`
<br>
This allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.

**Floats, positioning, and display WILL NOT work with flex**

## Good Resources
All encompassing guide: https://css-tricks.com/snippets/css/a-guide-to-flexbox/

Workflow Cheat Sheet: http://jonibologna.com/flexbox-cheatsheet/

Animated Tool: http://flexboxin5.com/

Flexbox Game: http://flexboxfroggy.com/







