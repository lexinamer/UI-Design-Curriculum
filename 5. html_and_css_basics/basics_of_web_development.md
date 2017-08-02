---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1MiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.fB8tRXLH9m6CN0c6hTdFgS79JRZcK70P6tkqnoOMvv0

title: >-
  Basics of Web Development
description: >-
  basics of web development
---
## What makes up a webpage?
- HTML: Hypertext Markup Language
- CSS: Cascading Stylesheets
- JS: JavaScript

![Screen Shot 2016-10-03 at 10.08.17 AM.png](https://s22.postimg.org/bpyftpe9d/Screen_Shot_2016_10_03_at_10_08_17_AM.png)

## How it works?
- HTML is how two computers speak to each other over the internet. Web sites are what they say.
- HTML is "spoken" by two computers:
  - Client: The client is used by the person surfing the net, such as the computer you are looking at right now.
  - Server: A server stores and distributes websites over the net. 

## The DOM
Web browsers implement what's called the [Document Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model), or "DOM", as the basis for interpreting content like HTML, XML, and SVG. The DOM is defined by the [W3C](http://www.w3.org) and can vary a little bit between browsers. It defines a "tree" structure for our webpage, resulting in "parent" and "child" elements. It also defines our events and lets us watch for them. This is critical for us when using JavaScript, as the DOM is the interface we use to target elements and watch for events.

## HTML
HTML uses markup tags to describe elements on a page. 
![html](http://www.keshkesh.com/wp-content/uploads/2014/07/html-syntax.png)

An HTML page has multiple elements that make it work. This is the basic setup. 
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>title</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js"></script>
  </head>
  <body>
    <!-- page content -->
  </body>
</html>
```

We can use the [Minimal HTML Document](https://www.sitepoint.com/a-minimal-html-document-html5-edition/) as a template

## CSS
CSS describes how HTML elements are to be displayed. It never affects the content or structure itself but specifically focuses on the presentation of content. 

![css syntax](http://raysensenbach.com/wp-content/themes/ray_v0.02/library/images/css1_01.png)

## Using CSS
There are three places where CSS can be specified for a document. In practice almost all styles are specified using external CSS files, though the other approaches can be useful in prototyping and a few limited use cases.

### External CSS file
By far the most common approach, creating a separate file to store CSS has the important advantage of being browser-cacheable. Browsers will download the file for the first visit but can reuse the same style sheet for all page loads afterwards without re-downloading it.

To link to an external CSS file, include a `link` element like the following in the `head` of your HTML document, replacing the CSS filename (the value of the `href` attribute):

```html
<link rel="stylesheet" href="css/style.css">
```

Note that you can also link to multiple CSS files (such as a CSS reset file, your site's overall theme, and perhaps a page-specific CSS file) using multiple lines like the one above, though it'll introduce more requests and will lead to slower page load times.

### In a `<style>` block
It's also possible to specify CSS styles in HTML files. Note that these styles will only apply to elements in the document where they're declared, and will be baggage that comes along every time the page is retrieved. On the upside, they only result in a single request, saving time on network round-trips (though the response will be larger than it would be with an external file).

In order to specify CSS in style blocks, use the following syntax in the `head` of your HTML document:

```css
<style type='text/css'>
    a { color: blue; }
    p { font-weight: bold; }
</style>
```

Note that all of the same CSS selectors and properties can be used; this is simply another way to include the same content that an external file could include.

### Inline with the element
Finally you can also include CSS as an attribute of the element itself. This approach only affects styles on individual elements, and comes with the same baggage that the `<style>` block approach above does. Nevertheless, it's available and sometimes useful for quick prototyping. The syntax here applied to a `p` block would look like:

```html
<p style="color: blue; font-size: 1.2em">Paragraph text</p>
```
