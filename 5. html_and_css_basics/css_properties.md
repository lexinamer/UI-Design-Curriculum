---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1NCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.-_sm3UroYMSyUm1e_r6gyDvsjGm0sG7Yv4GmAwGl-UU

title: >-
  CSS Properties
description: >-
  Let's get more control over our styles with the various properties of our web pages and elements that we can target in CSS.
---
## CSS and the Browser
Browsers apply what's referred to as a default style sheet that declares how elements should look when custom styles are not specified. Unfortunately default styles also aren't consistent across browsers and browser versions, so it's commonplace to include a stylesheet called a "CSS reset" to normalize your starting point. We will be using [Normalize.css](http://necolas.github.io/normalize.css/)


## Core components
CSS is applied to a document using *rules*, which describe two things: what styles should be applied (*properties*) and what they should be applied to (*selectors*). You will likely want to apply different styles for, say, links and standard text, or for headings and image captions. CSS provides a flexible way to do this.

Here's an example of a CSS rule that customizes the font of paragraph elements: 

```css
p {
  line-height: 1.1em;
  font-size: 1.2em;
  font-family: "Times New Roman";
}
```

## CSS rules
A CSS rule is the actionable unit that CSS is written in, and contains at least one *selector* (which specifies what the styles should be applied to) and one *declaration* (a statement made up of a *property* to target and a *value* to set that property to). 

It's possible for a single element to match multiple selectors, and have overlapping rules; in fact, this is quite common and can be a powerful technique for establishing simple and consistent styles when used correctly. For example, you can apply a single rule that customizes the `font-family` for an entire `body`, and all elements included in the body will inherit that `font-family` unless another more specific rule is provided.

How a rule is declared "more specific" than another rule is an important concept to understand which we will discuss later. For now, know it is referred to as **specificity.** In short, the more specific a rule is, the higher the specificity.


## Everyday CSS properties
CSS properties are used to specify what styles should be applied to a selection of elements. There are [a lot of different properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference), and CSS3 introduces many new ones. The properties you'll use will be heavily dependent on the project, but you'll normally use some form of:

- Layout and size properties (`display`, `margin`, `padding`, `width`, `height`, `border`, etc)
- Font properties (`font-size`, `font-color`, `font-family`, `line-height`, `text-align`, etc)
- Color properties (`background-color`, `color`, etc)

### Styling content: fonts
How text is presented greatly affects readability. CSS supports highly granular customization of text styles, including changing font families, font size, kerning, and weights.

- `font-family`: sets the font face used for text. This can be a specific font (e.g.: "Garamond", "Helvetica Neue"), a generic font family (e.g.: "serif", "monospace"), or a list of multiple choices. If multiple choices are given, the browser will go down the list until it finds a font that is available on the system, or fall back to the default font family if none of the font choices are available. For this reason, it's always good to end your `font-family` declarations with a generic font family. 
- `font-size`: the size of the text, which can be specified in several different ways: percentage, `em` or pixels.  
- `font-style`: used to set a font to either `italic` or `oblique`. 
- `font-weight`: sets the weight of a font. This can be just `bold`, or exact weight values (`100` - `900`, in increments of 100) for fonts that offer them. 

### Layout and sizing: layouts and box sizes
Layouts are perhaps the most error-prone CSS-related task and there are a lot of tools and best practices to be aware of. The CSS Layouts lesson covers both properties and practices related to CSS-based layouts. In short, important properties for layout-related tasks include:

- `display`: determines how the element's box will be positioned relative to other boxes
- `margin`: sets the margin around the element's box. You can provide a single value to `margin` to set the margin on all sides, or specify a specific side with `margin-top`, `margin-bottom`, `margin-left`, and `margin-right`. 
- `padding`: sets the padding around the element's box. This functions identically to `margin` - you can provide a single value or a specific side (`padding-top`, `padding-bottom`, `padding-left`, or `padding-right`).
- `width` and `height`: used to specify sizes of boxes (exact behavior depends on `display` value). `min-width`, `max-width`, `min-height`, and `max-height` are also helpful for sizing, especially for making layouts that accommodate a variety of screen sizes.

### Styling transitions: animations
Not all projects will have animations, but sometimes even subtle animations can have a surprisingly positive impact on the user experience. CSS3 adds many new tools for defining and managing animations, which we will learn about later. 

## Shorthand properties
*Shorthand properties* are a concise way to represent multiple related properties at once. For example, the `border` property allows us to configure values for `border-width`, `border-color`, and `border-style`. They're a convenient and quick approach to writing CSS, and also reduce the amount of information that needs to be sent to a user's browser. Using shorthand properties is usually a good idea, though there are a few gotchas to be aware of. The full list of shorthand properties includes:

- `animation`
- `background`
- `border`
- `font`
- `margin`
- `padding`

Certain properties also allow *shorthand values*. This means the way a shorthand property is applied is determined by the number of values used. For example, `margin` can be written as:

- `margin: 2em` - a margin of 2em on each side
- `margin: 2em 3em` - a margin of 2em on the top and bottom, and 3em on the left and right
- `margin: 2em 3em 4em` - a margin of 2em on the top, 3em on the left and right, and 4em on the bottom (uncommon form)
- `margin: 2em 3em 4em 5em` - a margin of 2em on top, 3em on the right, 4em on the bottom, and 5em on the left. Note that this moves in a clockwise direction, starting at the top.


## Common problems
The syntax of CSS is somewhat straightforward, but there are a number of places where developers can run into issues. Here are some common problems to look for if you're running into trouble:

- Make sure you're including semicolons at the end of all declarations. If you forget to include semicolons then properties after the forgotten semicolon may be ignored. Note that while it's not strictly necessary to add a semicolon after the last property in a rule, there's no reason not to and can prevent errors from occurring when you need to add new properties to the rule.
- Remember that browsers aren't consistent with their default CSS values, so just because something renders one way on your laptop doesn't mean it's going to look like that for everyone. Be explicit, and use a CSS reset to make sure that most defaults will be consistent across browsers.
- Remember that CSS assigns priority to selectors, called *specificity*. If a rule isn't being applied correctly, ensure that it's not being overwritten by another rule with higher specificity.

