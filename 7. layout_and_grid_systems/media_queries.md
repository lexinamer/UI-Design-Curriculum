---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE2MiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.J03f-p1cJPuKdUG1G6KtaEgX2Z24i02TULJhVJeXtwU

title: >-
  Media Queries
description: >-
  Learning how to use media queries
---
## Responsive web design
Often the hard part of implementing great layouts isn't finding the right CSS properties, but instead can be developing styles that work on all of the browsers and devices that your users may be visiting on. 

Responsive web design is a popular approach outlining how you can approach your layouts to work on as many devices as possible with relatively little implementation overhead.

The three core features of responsive web design are:
- Measure in ratios (the "flexible grid")
- Flexible images and media
- Media queries

### Best Practices
- Define all sizes as ratios so that they can scale up or down with the screen size. For fonts, this means using `rem` `em` not `px`. For layouts (columns, margins etc) this means using `%`, not `px`. For images, make sure they stay in their containers; `max-width: 100%` will usually accomplish this. 

- Under certain conditions (very small screens like certain phones, or very large ones like TV's) a single layout may not work well; this usually goes beyond an issue of scaling and requires alternative designs. You can use **media queries** to identify properties like the current width of the browser and trigger different styles based on the value. One common practice is to hide or stack columns on thinner screens.

Putting these two pieces together lets you accommodate for both dramatically different viewing environments (via media queries) and smaller variations within each environment (via fluid, ratio-based sizing).

### Mobile First Design
From a workflow perspective, many people prefer to start with the most constrained designs first (usually meaning the smallest screen size that you care about) because it forces you to think about what content is most important and reduces the probability of needing to do a design rework when you go from a larger to smaller design. As always, do what makes sense in your circumstance but this often saves headaches down the road.

## How Media Queries Work
- Media Queries are *conditional* rules in our CSS. They are **only** applied if the condition is true.
- Media Queries always start with `@` symbol followed by a single conditional.
- You aren't selecting an element, you are grouping a bunch of styles inside the conditional.
- For example: "If my screen width is greater than 320px then apply these styles."

```css
 section {
   background: blue;
 }
 
 @media (min-width: 320px) {
   section {
     background: red;
   }
 }
```

## Several ways to write media queries 

`Max-width`: This allows you to target specific elements that change ONLY when a screen shrinks below a certain size

```css
.left-col {
  float: left; 
}

.right-col {
  float: right; 
}

@media (max-width: 768px) {
  .left-col, .right-col {
     float: none;
  }
}
```

`Min-width`: This is the mobile first approach that will keep everything consistent ONLY until you change it at a larger screen size

```css
.left-col {
  background: red;
  height: 200px;
}

.right-col {
  background: blue;
  height: 200px;
}

@media (min-width: 768px) {
  .left-col, .right-col {
     float: left;
     width: 50%;
  }
}
```

`Min-width` and `max-width`: Lets you target a specific screen size between two points (such as tablet)

```css
.left-col {
  background: red;
  height: 200px;
}

.right-col {
  background: blue;
  height: 200px;
}

@media (min-width: 768px) and (max-width: 1024px) {
  .left-col, .right-col {
     float: left;
     width: 50%;
  }
}
```

## Common Screen Breakpoints
Breakpoints are the place at which the screen switches over to a new device or screen size. If you aren't taking a mobile first approach, there are a few standards to consider.

**Mobile**: 0px - 767px
**Tablet**: 768px - 1024px
**Desktop**: 1025px and up 

https://css-tricks.com/snippets/css/media-queries-for-standard-devices/
 
 - [Choosing between Min and Max Width](http://www.the-haystack.com/2015/12/23/choosing-between-min-and-max-width/)
 - [MDN Media Query Doc Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)


