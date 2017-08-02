---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE5NywiY29udGVudF90eXBlIjoiTGVzc29uIn0.OM-vtn51veNKh7fxnDSUbDXwzWoMKTEMYLO4kH27_Ys

title: >-
  CSS Basics
description: >-
  Basics information of CSS
---
## HTML and CSS
Unless they don't have any styling, all web pages will include both an HTML and CSS component. HTML and CSS together form what you see on a web page.

HTML is used to define what content should be presented and how that content should be structured on the page. HTML does not describe how that content should appear to users. 

CSS, on the other hand, never affects the content or structure itself but specifically focuses on the presentation of content. Web browsers use CSS to determine what color a background should be, what fonts to use, where to position different elements on the page, which elements need to be animated, and what the animations should look like, as well as many other presentation-related matters.

One of the benefits of the distinction between content and presentation is that styles can be modified without touching core content, and vice versa; similarly, upgrading the appearance of a site (changing a theme, for example) can be done largely by modifying CSS.

## CSS and the browser
Documents that are rendered, or presented, in a web browser are limited by what that browser knows how to do. A browser that hasn't been updated in three years, for example, won't know how to render a flashy animation that was only defined six months ago. CSS has a history of mixed support across the major browser vendors, though there's now a well-known [CSS standard](http://www.w3.org/standards/techs/css#w3c_all) that most vendors try to follow.

There are four "major" browsers used today[^1]: Google Chrome, Apple Safari, Microsoft Internet Explorer, and Mozilla Firefox. Support for the standard is becoming more consistent across these major browsers, though it's still wise to ensure that important styles work correctly on all popular browsers, which may include older versions. Luckily there are tools called [polyfills](https://en.wikipedia.org/wiki/Polyfill) that can help automate this and make it less painful for developers, and which properties work where is [well-documented](http://caniuse.com/).

Browsers also apply what's referred to as a *default style sheet* that declares how elements should look when custom styles are not specified. Unfortunately default styles also aren't consistent across browsers and browser versions, so it's commonplace to include a stylesheet called a "*CSS reset*" to normalize your starting point.

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

This rule applies a set of custom styles (specifically it sets the `line-height`, the `font-size` and the `font-family` properties) to all paragraphs (`p` elements) in the document. The "*p*" is referred to as a *selector*, and `line-height`, `font-size`, and `font-family` are all *properties*. Together, this block is referred to as a *rule*.

### CSS rules
A CSS rule is the actionable unit that CSS is written in, and contains at least one *selector* (which specifies what the styles should be applied to) and one *declaration*, a statement made up of a *property* to target and a *value* to set that property to. Here's how these components look when mapped out:

![CSS Syntax Diagram](https://s3-us-west-2.amazonaws.com/tiy-learn-lesson-assets/images/html/css-syntax-diagram.png)

Multiple selectors can be specified by placing a comma between them.

It's possible for a single element to match multiple selectors, and have overlapping rules; in fact, this is quite common and can be a powerful technique for establishing simple and consistent styles when used correctly. For example, you can apply a single rule that customizes the `font-family` for an entire `body`, and all elements included in the body will inherit that `font-family` unless another more specific rule is provided.

How a rule is declared "more specific" than another rule is an important concept to understand, and is referred to as [specificity](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity). In short, the more specific a rule is, the higher the specificity.

### CSS properties
CSS properties are used to specify what styles should be applied to a selection of elements. There are [a lot of different properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference), and CSS3 introduces many new ones. The properties you'll use will be heavily dependent on the project, but you'll normally use some form of:

- Layout and size properties (`display`, `margin`, `padding`, `width`, `height`, `border`, etc)
- Font properties (`font-size`, `font-color`, `font-family`, `line-height`, `text-align`, etc)
- Color properties (`background-color`, `color`, etc)

The CSS Properties lesson will run through some of these properties in greater detail.

### CSS selectors
Selectors are used to identify which elements a rule should apply to. There are three forms of basic selectors:

- *Tag selectors* are used for specifying specific elements by the tags they're declared with, and are written with just the name of the tag. For example, this rule will apply to all links:

```css
a {
  color: blue;
}
``` 
- *Class selectors* specify elements by the classes applied to them, and include a period before the class name. For example, this rule applies to elements where `class="highlight"`:

```css
.highlight {
  background-color: yellow;
}
```

- *ID selectors* specify elements by the element's ID, and are written with a hash symbol (`#`) before the ID. Note that a single document can only include a single element with a given ID. For example, this rule applies to the element where `id="header"`:

```css
#header {
  top: 0px;
  height: 75px;
  width: 100%;
}
```

Selectors can also be combined to be more specific using *combinators*; for example, it's possible to select "image elements in a header" or "paragraphs that have already been read in the 'chat' window" . See the CSS Selectors lesson for more information on this important feature.

## Using CSS
There are three places where CSS can be specified for a document. In practice almost all styles are specified using external CSS files, though the other approaches can be useful in prototyping and a few limited use cases.

### External CSS file
By far the most common approach, creating a separate file to store CSS has the important advantage of being browser-cacheable. Browsers will download the file for the first visit but can reuse the same style sheet for all page loads afterwards without re-downloading it.

To link to an external CSS file, include a `link` element like the following in the `head` of your HTML document, replacing the CSS filename (the value of the `href` attribute):

```html
<link rel="stylesheet" type="text/css" href="/css/mystylesheet.css">
```

Note that you can also link to multiple CSS files (such as a CSS reset file, your site's overall theme, and perhaps a page-specific CSS file) using multiple lines like the one above, though it'll introduce more requests and will lead to slower page load times.

### In a `<style>` block
It's also possible to specify CSS styles in HTML files. Note that these styles will only apply to elements in the document where they're declared, and will be baggage that comes along every time the page is retrieved. On the upside, they only result in a single request, saving time on network round-trips (though the response will be larger than it would be with an external file).

In order to specify CSS in style blocks, use the following syntax in the `head` of your HTML document:

```css
<style type='text/css'>
    a { color: blue; }
    #footer {
        bottom: 0px;
        width: 100%;
    }
</style>
```

Note that all of the same CSS selectors and properties can be used; this is simply another way to include the same content that an external file could include.

### Inline with the element
Finally you can also include CSS as an attribute of the element itself. This approach only affects styles on individual elements, and comes with the same baggage that the `<style>` block approach above does. Nevertheless, it's available and sometimes useful for quick prototyping. The syntax here applied to a `p` block would look like:

```html
<p style="margin: 1%; font-size: 1.2em">Paragraph text</p>
```

Note that inline styles can be specified on any element, not just `p` elements.

[^1]:http://gs.statcounter.com/
