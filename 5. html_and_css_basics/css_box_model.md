---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1NywiY29udGVudF90eXBlIjoiTGVzc29uIn0.DPOeL5-ERnZ6qPIkpBk6jEXvkrDQbg6NzsE5gD_GTH0

title: >-
  CSS Box Model
description: >-
  Notes on the how content, padding, margin, and border are related.
---
## CSS Box Model

### The box model
The "bounding boxes" referred to above are a part of the *box model* used for specifying the size and position of all HTML elements. All HTML elements are rendered in the document as a box with a certain width and height. Each element's box is made up of a series of smaller nested boxes.

![box model](http://image.slidesharecdn.com/css-boxmodel-130811120108-phpapp02/95/css-box-model-2-638.jpg?cb=1376222562)

There are four smaller boxes that make up each element's box, each of which can be sized using CSS properties.
- The *core content area* is where text, images, etc will appear. This is the innermost box and can be sized using `width` and `height` rules.
- The *padding* is the blank space between the content and the border, and can help give individual elements breathing room beside the rest of the content on the page. Padding can be adjusted using `padding` rules.
- The *border* is the region that marks the visual edge of the box; the `background-color` of the box, for example, will not extend beyond the border. The border's width, color, and style can be adjusted all at once using the single `border` shorthand property, or individually using `border-width`, `border-style`, and `border-color`.
- Last but not least, the *margin* is the blank space between the border of the element and the next element. Margins are similar to padding but are positioned outside of the visual area of the element. Margins can be styled using the `margin` property.

When it comes to specifying sizes, both *absolute* (`px`) and *relative* (`%` and `em`) are usually valid but make sense in different circumstances. Make a conscious decision about which should be used based on what you're trying to accomplish and be consistent unless you have a good reason not to be. When it comes to layouts, relative sizes are often preferred since they'll accommodate a broad range of screen sizes.

### Helpful Hints
- Everything in HTML is a box
- All elements can have from one to four values (top, right, bottom, left) 
- 4 different parts to every box
    + content
    + padding
    + border
    + margin

- 2 types of elements
    + block-level elements (container/parent elements)
        * will always be the full width of their container (or browser)
        * proud parents 
            * use them to hold other things (like to have children)
            * proud because they like to swell up and be big and wide (they don't like to be next to things)
    + inline-elements (text content and images)
        * anchor tags and spans
        * will only be as wide as their content
        * bratty teenagers 
            * like to be next to their friends (they will line up next to each other)
            * bratty because they don't respond to  your request
                - doesn't take width or height
                - will do left/right margin, but not top and bottom

#### Content
- the size of the box is the content, not including padding, border, margin

#### Height
- height and width affect content in box model
- fixed height can cause
    + overflow
    + overlap
- If you don't fix a height, it will be as tall as its content

#### Padding
- padding size gets added to the overall size of the box we could see
- background color is applied to padding and content
- The `box-sizing` property is used to alter the default CSS box model used to calculate width and height of the elements. 
   - `box-sizing: content-box`: The width and height properties are measured including only the content, but not the padding, border or margin
   - `box-sizing: border-box`: The width and height properties include the content, the padding and border, but not the margin. 

#### Margin
- margin is space that gets added to the area outside of the element 
- the margin is transparent and doesn't include the background color


