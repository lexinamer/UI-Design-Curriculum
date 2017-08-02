---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1OSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.vRIT92hLHQjH7zTWS60KSLTtZmRASWWSqQyQ2EigJIk

title: >-
  CSS Layouts
description: >-
  A large part of our presentation is *where* elements are on our web page. Let's learn to use CSS for controlling our page layouts. 
---
In addition to styling, one of the most important capabilities of CSS is the ability to define flexible layouts for our content. Layouts have a tremendous impact on the usability of a website and designing something that will work across the full range of browsers and devices takes some practice and awareness of common challenges and pitfalls. 

Once completed, a well-designed layout will make it possible to add and modify content without needing to adjust the layout to accommodate the new material. 

## Common CSS properties
Generally speaking, the art of creating an effective layout involves specifying positions of elements, as well as how those elements should adjust under different circumstances (changing screen / window dimensions, for example). Elements are defined by a *bounding box* that occupies a location in your layout. CSS layout properties are all about defining the location and interaction between elements' bounding boxes. 

### Display
The CSS specification states that the `display` property defines, among other things, how the box participates in the parent formatting context. In other words, it defines the element's *role* in the layout. There are two primary roles: `block` (meaning it occupies the entire horizontal space, such as a section of a page or container) and `inline` (meaning it occupies a portion of the horizontal space, such as column of text or embedded image).

- `display: block` - the element should, by default, start on a new line and occupy the full width of the parent element, but also respect explicit `width` and `height` values. This is the default for elements like `div`, `p`, and the header elements (`h1`, `h2`, etc).
- `display: inline` - the element should, by default, occupy only the required amount of space to present all of its content. Other content can be placed before or after it horizontally. Inline elements cannot have an explicitly defined `width` or `height`. This is the default for elements like `span` and `a`.
- `display: inline-block` - a useful hybrid of block and inline display types, which allows for `width` and `height` to be specified but will also allow other elements to appear before or after it horizontally. This is the default for elements like `button` and `select`.
- `display: none` - the element should not be visible and should not occupy space in the layout. Note that there is also a `visibility` property that can also hide items, though they will still occupy space. `display: none` is sometimes useful when you are creating mobile versions of sites.
- `display: flex` - a newer property on the scene that can be a bit harder to find dependable resources on. Flex, or flexbox, properties approach layouts slightly differently and allow child elements to be ordered, wrapped, sized, and aligned relative to other elements in the same flexbox.

### Position
The `position` property, along with `float`, is used to define how an object's location is described to the browser. All elements default to `position: static`, but this can almost always be changed if needed. Once changed, the position is described using the `top`, `bottom`, `left`, and `right` (positional) properties.

`position: static` - the element is not positioned in any special way; it is always positioned according to the normal flow of the page. This is default.

<iframe height='265' scrolling='no' src='//codepen.io/lexinamer/embed/QKkkLw/?height=265&theme-id=0&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/lexinamer/pen/QKkkLw/'>Position Static</a> by Lexi Namer (<a href='http://codepen.io/lexinamer'>@lexinamer</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

`position: relative` - the element is positioned relative to its normal position. It is probably the most confusing and misused. What it really means is "relative to itself". 

If you set position: relative; and don't do anything else, it will be exactly as it would be if you left it as position: static; But if you DO give it some other positioning attribute, say, top: 10px;, it will shift it's position 10 pixels DOWN from where it would NORMALLY be.

<p data-height="265" data-theme-id="0" data-slug-hash="gwBBYE" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/gwBBYE/">Position Realtive</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

`position: absolute` - This is a very powerful type of positioning that allows you to literally place any page element exactly where you want it. The element's position is *ignored* and overwritten by the positioning attributes top, left bottom and right to set the location.

They are taken out of the normal flow and do not affect other elements but are positioning in relation to the parent element with positioning. If there is no parent element, it will default to the top of the page. 

<p data-height="367" data-theme-id="0" data-slug-hash="XjxxNZ" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/XjxxNZ/">Position Absolute</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

`position: fixed` - the box's position is treated just like `position: absolute`, but will also be locked to that position with respect to a particular point of reference (usually the browser's viewport), meaning that the element will maintain it's position even if the user scrolls. 

It will go on top of whatever content you have above it because it doesn't care about positioning. 

<p data-height="265" data-theme-id="0" data-slug-hash="WGaaXx" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/WGaaXx/">Position Fixed</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

### Float
The float property, like the `position` property above, describes how the browser should interpret the positioning of the element. `float` is used for extracting elements from the normal flow and moving them to the left or right of other elements in their parent's box. For example, wrapping text around an inline image is typically achieved by floating the image.

- If you float a child element the parent element will collapse. If you don't have any padding, it will look like it disappears entirely.
- If you add the property overflow:hidden to your parent div, it will prevent it from collapsing. Kind of a hack for fixing parent/child floating issue.
- You won't notice the parent element has collapsed unless you have a background color.

`float: left` means that the element should be moved to the left of non-float content, and `float: right` means that it should be moved to the right of non-float content. Floats will move in the specified direction until they reach the edge of the box or another floating element.

Floats are often used to create multi-column layouts or to position particular elements. Note that you'll need to be familiar with the `clear` property (introduced below) if you want to use flows to define page layouts.

<p data-height="265" data-theme-id="0" data-slug-hash="vXVVwB" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/vXVVwB/">Floats</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

### Clear
The clear property is used for indicating to the browser how a particular element should position itself relative to nearby floating elements. It's used exclusively in conjunction with the `float` element above, though they're usually applied to different elements.

`clear: left` means the element should be positioned below elements that are `float: left`, and `clear:right` is the same for elements that are `float: right`. You can also specify `clear: both`, which covers both cases.

<p data-height="341" data-theme-id="0" data-slug-hash="bwmmPg" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/bwmmPg/">Floats and Clear</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

### Vertical and Horizontal Centering
- Centering is a tricky thing that can be achieved numerous ways depending on what you want to be centered, what properties it has, and whether you want to center it vertically, horizontally, or both 

##### Horizontally
- If inline element, you can use text-align: center
- If block element, give it a margin: 0 auto (this will work no matter the height or width but you cant center a floated element [Here is a good resource](https://css-tricks.com/float-center/) 

#####Vertically
- There are many ways but I like this 3 line trick that works a lot of the time found [here](http://zerosixthree.se/vertical-align-anything-with-just-3-lines-of-css/)
  `position: relative;
  top: 50%;
  transform: translateY(-50%);`
- There is also a complete centering guide by [CSS Tricks](https://css-tricks.com/centering-css-complete-guide/)

### Margin and Padding
`margin` is the space around the outside of a box that should not be used for other boxes; it will be rendered as whitespace between the border of the box and the next element.

`padding` is the space between the content of the box and the border that should not be used for other content; it too will be rendered as whitespace, though *inside* of the border in this case.

Another useful trick: when the `auto` value is specified, the `margin` property will split the available space between left and right margins, effectively centering the element. This is handy trick and usually the easiest way to center block-level elements horizontally.

### Min and Max
Sometimes it's useful to be able to specify minimum or maximum heights and widths. For example, if you specify that the navigation bar on your website should be `30%` of the page width, all is fine and dandy until someone views the page on their watch and 30% becomes a very small amount of space. In cases like this, you'll often want to define a `min-width` to ensure there's at least X pixels available. This will work alongside a defined `width` (or `height` in the case of the min/max height properties).
