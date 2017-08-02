---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1NiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.6rWgrQTVINxgSQGtcY-Si5plr7sOCdwwB6Tmt1FOy1w

title: >-
  Divs, Ids, and Classes
description: >-
  Learning to control HTML and CSS
---
## Content Containment

Part of HTML's purpose is to provide a scaffold for your web page. This means content should be organized in a logical manner, and HTML provides lots of tools to help us accomplish this effectively. 

Without utilizing other resources like CSS, HTML provides us with a single shape to work with: a rectangle. We refer to HTML's invisible organizational rectangles as "divisions", or `div`s. `div` elements extend fully across the web page and allow you to organize content based on its purpose or location on the web page. `Div` elements aren't visible without styling. Most divs will include attributes that aid in styling them.

```html
<div>
   <h2>This is a header for this section</h2>
   <p>Here is a paragraph within the section<p>
   <p>Here is another paragraph</p>
</div>
```

We can style the `div` like we can any other element. `div`s are not visible inherently, and changes size depending on the content within it. If there is no content inside the `div` we can add styling to force them to appear on the page. 

```html
<div></div>
```

```css 
div {
  width: 100%;
  height: 200px;
  background-color: red;
}
```

**Note:** While it can be useful while learning to create blank `div`s and give them specific sizing constraints, this can be problematic (especially if you set an absolute height) when you actually add content because, depending on the size of the device a user is using, it may cause the content to look distorted. The best practice is to let the `div` automatically size based on the content and not the other way around. 


## Classes and Ids
We need ways to describe content in a an HTML document. The basic elements like `<h1>`, `<p>`, and `<div>` will often do the job, but our basic set of tags doesn't cover every possible type of page element or layout choice. For this we need ID's and Classes. 

For example `<div id="header">`, this will give us the chance to target this specific `div` to have certain properties. Or perhaps we have boxes in our sidebar for keeping content over there separated in some way: `<div class="sidebar-box">`. This can also work with any HTML elements, and lets us quickly target specific elements of the page. For example, `<p class="red-text">This is red text</p>`.

Think of classes and Id's as a naming device to target individual elements and get more control. 

### IDs
IDs are unique:
  - Each element can have only one ID
  - Each page can have only one element with that ID

Your code will not pass validation if you use the same ID on more than one element. Validation should be important to all of us, so that alone is a big one. 

```html
<div id="header">This would be the header container</div>
The id header CANNOT be used again
```

In CSS, IDs are called with a hashtag: `#header { background-color: red;}`

### Classes
Classes are NOT unique: 
  - You can use the same class on multiple elements.
  - You can use multiple classes on the same element.

Any styling information that needs to be applied to multiple objects on a page should be done with a class. 

```html
<div class="article-box">This could be one article</div>
<div class="article-box">This can be used again and again</div>
```

In CSS, classes are called with a dot: `.article-box { color: red;}`


## Harnessing Classes and Ids
Classes and ID's don't have any styling information to them all by themselves. They require CSS to target them and apply styling.

### ID's have special browser functionality
Classes have no special abilities in the browser, but ID's do have one very important trick up their sleeve: they can function as anchor links, or links within a page. If you have a URL like http://yourdomain.com#comments, the browser will attempt to locate the element with an ID of "comments" and will automatically scroll the page to show that element. 

This is an important reason right here why having ID's be absolutely unique is important. So your browser knows where to scroll!


### Elements can have BOTH
There is nothing stopping you from having both an ID and a Class on a single element. In fact, it is often a very good idea. 

`<div id="footer" class="secondary-box">`
It has a class applied to it that you may want for styling all secondary boxes on the page, but it also has a unique ID value that is useful for direct linking. Now I can link directly to a particular comment on a particular page easily.


### CSS doesn't care
Regarding CSS, there is nothing you can do with an ID that you can't do with a Class and vice versa. 

### Javascript cares
JavaScript depends on there being only one page element with any particular, or else the commonly used getElementById function wouldn't be dependable. 

### If you don't need them, don't use them
Classes and ID's are very important and we rely on them everyday to do the styling and page manipulation that we need to do. However, you should use them judiciously and semantically.

This means avoiding things like this:
`<a href="http://google" class="link">Google</a>`

We already know this element is a link, it's an anchor element.There is no particular need here to apply a class, as we can already apply styling via its tag.


[CSS Tricks Resources](https://css-tricks.com/the-difference-between-id-and-class/)


