---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1NSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.xMCPxWQMfj6fw2m8EbzsYwHk9zxFaaa60Q2wBDMh6lw

title: >-
  Links and Images
description: >-
  Learn how to use links and image optimization
---
## Links
A link has two ends -- called anchors -- and a direction. The link starts at the "source" anchor and points to the "destination" anchor, which may be any Web resource (e.g., an image, a video clip, a sound bite, a program, an HTML document, an element within an HTML document, etc). One of the most common things newcomers to HTML get confused about is linking to other pages and sites, especially when absolute and relative paths come into play. 

### Relative Links
A relative link generally sends the user to somewhere within your site. You can tell it is a relative link because it isn't a full website address (A full website address includes http://). 

`<a href="linkhere.html">Click Me</a>`

### Absolute Links
An absolute path does provide the full website address and would send the user to an external site away from your website. 

`<a href="http://google.com>Google</a>`

In both examples, the `linkhere.html` is the website address and `click me` or `Google` is the text that would be displayed on the website for the user the click. 

### Linking to a new tab
A good rule of thumb is to have any absolute opens in a new tab while moving to pages between your site opens in the same tab. To have a page open in a new tab, we use the target attribute to specify where to open the linked document:

`<a href="http://www.google.com" target="_blank">Google</a>`

### Linking to a stylesheet
To link to a CSS stylesheet, the syntax is slightly different. Instead of using `a href` you use the property `link href` to indicate that it is linking to a stylesheet and not an external link. You should also include what type of file you are linking to through the rel attribute as seen below. This type of link does not require a closing tag. 

`<link href="css/style.css" rel="stylesheet">`


## Images
Images do not include a closing tag and are written through the `<img>` tag. You can use both absolute and relative URLS within your images, but remember that if you link to an image outside of the project and it is taken offline, your image link will break. Also, image links are case sensitive and must include the exact path and name of the image. 
`<img src="url">`

It is always important to include an `alt` attribute to provide alternative information for an image if a user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader).

`<img src="url" alt="description of image">`

### Images as Links
Images can also be links and can be styled as such. To create a linkable image, you would wrap the image in a link tag and include the image instead of the url. 

`<a href="about.html"><img src="images/image.jpg"></a>`

### Image Optimization
In order for images to load quickly, they should be the smallest file size possible. The easiest way to reduce the file size of an image is to make it no larger than 1920px width (the most common screen size) and at 72dpi (dots per inch). This can be done using the Apple Preview software include on your computer. 

Another trick to reducing image size is to use [Tiny JPG](http://tinyjpg.com) which optimize your images with a balance in quality and file size. 

We will get more into image editing later, but all images should be less than 1mb in size as the absolute largest. 


### Background Images
- You can easily add background images using CSS. It is done through the `background-image` property that sets one or more background images for an element.
- The background of an element is the total size of the element (most often will be a `div`), including padding and border (but not the margin). Remember, `div`s are inherently invisible so you may need to set parameters in order to make the background image appear.
- By default, a background-image is placed at the top-left corner of an element, and repeated both vertically and horizontally. You should also always add a backup color in case the image can't be read. 

```css
body {
    background-image: url("../images/main-bg.jpg");
    background-color: red;

 /* These next lines can control the size and display */
    background-size: contain (or cover);
    background-repeat: no-repeat;
}
```
