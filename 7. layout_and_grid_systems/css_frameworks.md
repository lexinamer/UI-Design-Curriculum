---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE2NCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.P7hpSCk0kRb_lR8-gcJbA6tpqPAPXAbbIIuUiImh0Tg

title: >-
  CSS Frameworks
description: >-
  overview of CSS frameworks
---
### CSS Frameworks
- In the world of web design,  a framework is defined as a package made up of a structure of files and folders of standardized code (HTML, CSS, JS documents etc.) which can be used to support the development of websites, as a basis to start building a site.

- The aim of frameworks is to provide a common structure so that developers don’t have to redo it from scratch and can reuse the code provided. 

- Front end frameworks usually consist of a package made up of a structure of files and folders of standardized code (HTML, CSS, JS documents etc.)

- Two Types 
  - Simple: 960 Grid, Susy, Base, Toast
  - Complex: Bootstrap, Foundation, Skeleton 

- How do choose the right one? [What are Frameworks](http://www.awwwards.com/what-are-frameworks-22-best-responsive-css-frameworks-for-web-design.html)


### The Way it Works
Container 
```html
<body>
   <div class="container">
   ---more content---
</body>
```

Rows 
```html
<div class="container">
   <div class="row">
   </div>
</div>
```

```html
<div class="container">
   <div class="row">
      <div class="olumn-info">content</div>
      <div class="olumn-inf">content</div>
   </div>
</div>
```
