---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1MywiY29udGVudF90eXBlIjoiTGVzc29uIn0.RaAahn5KZiNUVKGnkiD_UPGA29sZxhIKhojrUzhvS1I

title: >-
  HTML Elements
description: >-
  Learning the basics of HTML
---
## The Importance of Content
We've covered the basics of a web page - the required elements, content, and metadata, and how to include other resources in your page. Let's get to the fun stuff now: your own content! HTML content provides the scaffold for your whole web page and is where your creativity really gets to come out.

It's important to remember as we start learning how to add content that HTML is intended to be your web page's skeleton. When designing the HTML for your web page, you should be concerned about intent and purpose, not color, shape or size.

## Text Content
The most common type of content on the Web is text. Every site needs text, whether it's a news article, an image caption or a dynamic chatroom. Let's talk about the different types of common text elements.

`p`: We've seen this element already. `p` stands for "paragraph" and is intended for independent portions of text. Paragraph elements will often include extra space before and after the element when they're rendered.

```html
<p>This is a paragraph of text. It can just be one sentence or a whole bunch of sentences.</p>
<p>Here's a another paragraph element. See how these two elements are spaced apart?</p>
```

`h1, h2, h3, h4, h5, h6`: "H" stands for "Header". These `h`-elements (1-6) are intended to be headers for your web page or individual sections of it. `H1` is the largest of the header elements and should be reserved for top-level headers, while `H2` - `H6` get progressively smaller by default and are intended for subsections or content titles. 

```html
<h1>HEADERS</h1>
<h2>Why use headers?</h2>
<p>Headers are used for content that should be extra-visible and is important for labelling your page's content.</p>
<h3>Header sizes</h3>
<p>The size of each header will vary across browsers.</h3>
<h3>REMEMBER</h3>
<p>Headers should be used to indicate titles & sections, NOT just for bigger/smaller text!</p>
```

`span`: The "span" element lets you select text "inline", or embedded within other elements. Span elements are often used to single out words that will need to be styled or acted on by an external resource (like CSS or Javascript).

```html
<p>We'll style <span class="first">this text</span> as red and <span class="second">this text</span> as blue.</p>
```

`pre`: Pre elements are used for displaying "preformatted" text. This means text that won't get the default styling from your browser. Pre elements are most often used for displaying code in your web page.

```html
<p>Let's look at some code:</p>
<pre>
  <h3>SAMPLE CODE</h3>
  <p>Here's some sample code.</p>
</pre>
<p>That was a great sample!</p>
```

`blockquote`: Block quotation elements are used to indicate a quoted block of text. This is generally rendered as indented on your web page to indicate that it should stand alone.

```html
<p>Consider this quote from Edward Dijkstra:</p>
<blockquote>Simplicity is prerequisite for reliability</blockquote>
<p>It's good to remember to keep your code simple so others can work on it.</p>
```

`em` and `strong`: These two elements are both used to note important content, but each act in a different way. The `<strong>` element denotes important text, but does not affect meaning. This is often displayed as bold. The `<em>` element denotes important text and affects the meaning of the content by saying that it should be read/spoken with emphasis. This is often displayed in italics. 

```html
<p><strong>WARNING</strong>: Acid will burn you. Do <em>not</em> drink any acid.</p>
```

`br`: The "*break*" element isn't strictly a text element, but it's used with text content. `br` inserts a line break in your web page. It shouldn't used to simply separate text (that's what a new `p` element is for), nor should it be used for pushing elements down in your layout (we'll discuss better ways to do this soon).  However, within a paragraph element, `br` is an effective way to separate content. `br` is a void element, so it doesn't use a closing tag. This element should be used sparingly. 

```html
<p>
  Here's a bunch of text. We're including a super important link we want on its own line.
  <br>
  <a href="http://www.important-site.com">Important Link</a>
  <br>
  We can use the break element to put the link on its own line without all the extra spacing new paragraph elements would cause.
</p>
```

## Attributes & Special Content
Let's discuss another important part of an HTML element: *Attributes*. We've seen attributes in some of our examples but haven't discussed them in-depth yet.

HTML elements often need data beyond their content. To supply this data, we can use "key-value" pairs inside the opening tag of the element. These pairs are referred to as "attributes" and use the following patten: `key="value"`. Attributes are optional for some elements and mandatory for others. Here's an example of an anchor element using attributes:
```html
<a href="http://www.theironyard.com">The Iron Yard's Homepage</a>
```
Generally, consider the purpose of the element you're using - does it need extra data to fulfill its purpose? It probably has mandatory attributes to provide that data. 

Let's look at two very common elements that require the right attributes to function properly: anchor & images.

`a`: The `a` element, short for "*anchor*", provides a hyperlink to another web page or to another location on the current web page. Hyperlinks are the backbone of the Web and make it possible to easily navigate between content. Hyperlinks (usually just called "links") require an "*href*" attribute ("Hypertext REFerence") so that they know where to direct the user when they're clicked. The anchor element will generally be rendered as its content, but distinctly colored and sometimes underlined. An `a` element without an `href` attribute does nothing - it will be styled in a special way, but acts like plain content otherwise.[^2]

```html
<p>Click <a href="www.theironyard.com">here</a> to visit The Iron Yard's homepage.</p>
```

`img`: `img` is an abbreviation of "image", and provides the ability to add pictures to your webpage. The `img` element requires a `src` ("SouRCe") attribute pointing at the desired image's location. This can be on your current server or on another web page. It's not required, but it's always a good idea to include the `alt` attribute as well. `Alt` provides "ALTernative" text that will be displayed if your image can't load or will be read out loud as a description of the image for people who can not see. `img` is a void element and doesn't use a closing tag.

```html
<img src="red-panda.jpeg" alt="Adorable red panda cub laying in grass.">

<a href="http://cool-site.com"></a>
```
