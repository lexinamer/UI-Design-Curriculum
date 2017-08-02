---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE2NSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.DWQCOGQ7fI_Sr2u-Cy7YcQBOpq_z7XqZvsQ4NKw-jsU

title: >-
  Basics of Web Typography
description: >-
  Basics of web typography 
---
# Web Typography
Good typography is important in any website or application you make. It increases the readability of our websites, helps make it accessible or not, and evokes mood and tone (which we will learn about more in depth next week).  There are a few basics of typography in relation to how we treat it as web designers and developers. 

### HTML Type Tags
- The Heading tags (`h1`, `h2`, `h3`, `h4`, `h5`, `h6`) are there to convey the meaning and importance of the content on the page.
- The Paragraph tags (`<p>`) are there for paragraphs and the "body copy" of your web page.

### Line Height and Spacing
- Your line height should never be below `1.6`. The best line spacing for paragraph readability is between 1.6 and 2.0. Keep line-height unitless. 
- The minimum font size should be 16px.
- There should be between 50 and 75 characters per line of reading content.
- Setting a `max-width` such as 960px on the body of your page will prevent the content for stretching too wide.

### Basic Rules
- Don't use `text-align:center` on large amounts of body copy.
- Never use more than 2 fonts in your projects
- Google Fonts has a great selection of free fonts with a pairing guide.

### Font Weights
Font weights are the weight of the font face's appearance. How dark or think it looks. Font faces are the Typeface itself.

Many fonts that you get will come with different weights that you can use. Whenever you can, use the font weight number. The font weight "bold" setting just thickens the original font.

- Bold = 700
- Normal = 400
- Light = 300


### Icon Fonts
Icon fonts are awesome because they allow you to add little icons and style them like you would any other font. 

[Font Awesome](http://fontawesome.io/) is probably the best one around and don't forget to link to the font first before you can use it. 


### Type Sizes
Px, em and rem are all units of length used to define the size of elements on a webpage. You can use them on divs, margins, padding, and so on.

`px`: pixels are the same size regardless of the size of anything else. In practice, they aren’t the same length everywhere because different devices treat them differently, but on each device a pixel is always the same. 16px on your laptop monitor is not the same as 16px on your iPad. Pixels are absolute but not consistent.

`em`: Ems are a relative measure of length. The size of an em is relative to the font-size of its parent element. If you have a `<div>` with the font-size set to 16px, and a `<p>` element inside that div with a font-size set to 2em, the font-size of text in the `<p>` will be 32px.

`rem`: Ems have a problem. Because everything is sized relative to its parent element, the meaning of an em changes as elements are nested. Rems are always relative to the font-size of the <html> element. It doesn’t matter how deeply nested an element is, its rem lengths will always be a proportion of the font-size of `<html>`.

https://www.futurehosting.com/blog/web-design-basics-rem-vs-em-vs-px-sizing-elements-in-css/


### Responsive Typography
Responsive typography is a difficult thing to accomplish, especially when using units of measurements that are more static (px instead of %). There are a few ways to ensure a good reading experience for users. 

1. Increase font-size and line-height of your body copy as screen sizes increase. Typically, this occurs during the breakpoints. 
2. Use a modular scale for your typography. A modular scale, also called typography scale, is a tool to help you pick good typography sizes based on a ratio: www.modularscale.com
3. Always write typography with relative units instead of pixels. This means using em and rems. 
4. [Fluid Typography](https://css-tricks.com/snippets/css/fluid-typography/). (This seems like a great idea but I've never used it and it might be experimental...)
5. [Typi](https://zellwk.com/blog/typi/) is a Sass library that allows you to set up font-size and line-height properties of all your typographic elements in separate Sass maps. 

### Typographic Hierarchies
Typographic hierarchy is a system for organizing type that establishes an order of importance within the data, allowing the reader to easily find what they are looking for and navigate the content. 

It helps guide the reader’s eye to where a section begins and ends, whilst enabling the user to isolate certain information based on the consistent use of style throughout a body of text.

http://webdesign.tutsplus.com/articles/understanding-typographic-hierarchy--webdesign-11636
