---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMzgwOCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.H6eyZqvwSRhJ6HgfKL8TlU018gj_koFmREGdx7jiyFc

title: >-
  Bootstrap and Skeleton CSS
description: >-
  Learning two popular grid frameworks
---
# Bootstrap 
- Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web.
- Built by the team at Twitter, open sourced and has now gone through 3 versions and about to release v4
- Includes a ton of components, a great grid system, and is easy to get started, though it is not very lightweight and can slow a site down.  

### How to Use
1. Go to (http://getbootstrap.com/)
2. Click on "getting started"
3. Use the included files or download the entire folder and start your project
  - [Bootstrap CDN](https://www.bootstrapcdn.com/)
  - [Bootstrap Tutorial](https://www.toptal.com/front-end/what-is-bootstrap-a-short-tutorial-on-the-what-why-and-how)

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

Columns (= 12)
```html
<div class="container">
   <div class="row">
      <div class="col-md-6">content</div>
      <div class="col-md-6">content</div>
   </div>
</div>
```

### More hints and tips
- Built in components: http://getbootstrap.com/components/
- You can specify how the columns break on the different devices by adding an additional class
`<div class="col-xs-4 col-md-6">content</div>` 




# Skeleton
- Skeleton is a popular, easy to use, responsive boilerplate
- Very lightweight with under 400 lines
- Great for smaller projects where you dont need all the utility of larger frameworks

### How to Use
1. Go to (http://getskeleton.com/)
2. Click on "download"
3. Use the included Skeleton.css file in your project
4. Link to that file in your HTML pages

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

Columns (= 12)
```html
<div class="container">
   <div class="row">
      <div class="two columns">content</div>
      <div class="ten columns">content</div>
   </div>
</div>
```

### More hints and tricks
- There are few components such as fonts and buttons: http://getskeleton.com/#typography
- It automatically collapses to a single column and this isn't customizable
- There is an unofficial Sass version: https://github.com/whatsnewsaes/Skeleton-Sass (its in beta so be forewarned)
