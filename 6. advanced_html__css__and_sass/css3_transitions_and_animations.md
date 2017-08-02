---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE3OCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.WGWZETAMARz9w5EY51v1rVI-ak7RysDtUM3BMQARS88

title: >-
  CSS3 Transitions and Animations
description: >-
  Covers a variety of techniques for CSS3 Transitions and Animations
---
# What are CSS Transitions and Animations?
One evolution with CSS3 was the ability to write behaviors for transitions and animations. Front end developers have been asking for the ability to design these interactions within HTML and CSS, without the use of JavaScript or Flash, for years. Now their wish has come true.

With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted.

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.


# CSS Transitions
CSS transitions, provide a way to control animation speed when changing CSS properties. Instead of having property changes take effect immediately, you can cause the changes in a property to take place over a period of time. 

For example, if you change the color of an element from white to black, usually the change is instantaneous. 

Elements with a transition must be in a state of change for the transition to take place. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes. 

![transitions](https://developer.mozilla.org/files/4529/TransitionsPrinciple.png)

<br>

### A note about the transform property
The `transform` property allows you to visually manipulate an element by `skewing`, `rotating`, `translating`, or `scaling`. 

You may often see this in conjunction with the `transition` property to make an object grow, shrink, or rotate. This is also how our magic 3 line vertical centering works with layout. 

An awesome article about it: 
https://css-tricks.com/almanac/properties/t/transform/

<br>
## How do transitions work?
First you need to write your HTML- in this example we are going to just make a box grow, change colors, and rotate 

```html
<div class="box"></div>
```

Add your styling to make your default box (blue and square)
```css
.box {
    width: 100px;
    height: 100px;
    background-color: blue;
}
```

Now we need to add the transition property to give it the animation parameters for how long we want the transition to take place.

Note that we also used a transform property integrated

```css
.box {
    width: 100px;
    height: 100px;
    background-color: blue;
    transition: width 2s, height 2s, background-color 2s, transform 2s;
```

Now we make the magic happen with the hover states. First we add our hover elements like normal.
```css
.box:hover {
    background-color: pink;
    width: 200px;
    height: 200px; 
```

Now we add the transform property to make it rotate while the transition takes place.
```css
.box:hover {
    background-color: pink;
    width: 200px;
    height: 200px;
    transform: rotate(180deg);
}
```

<p data-height="280" data-theme-id="0" data-slug-hash="GqGrBK" data-default-tab="result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/GqGrBK/">CSS Transition Example</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<br>
## Another example of doing a color change with a transition on hover

<p data-height="469" data-theme-id="0" data-slug-hash="xOzpqE" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/xOzpqE/">CSS Transition Example Color Change</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
<br>
### So what css properties can we transform?
There are a ton and you get to decide! Mozilla has a [list](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties) though its ever-changing so make sure to check back frequently. 
<br>

## Transition Properties
There are four transition related properties: 
- `transition-property` Specifies the name or names of the CSS properties to which transitions should be applied. Only properties listed here are animated during transitions; changes to all other properties occur instantaneously as usual.
- `transition-duration` Specifies the duration over which transitions should occur. You can specify a single duration that applies to all properties during the transition, or multiple values to allow each property to transition over a different period of time. Example: `transition-duration: 6s;`
- `transition-timing-function` Specifies a function to define how intermediate values (or actions) for properties are computed. This in essence lets you establish an acceleration curve, so that the speed of the transition can vary over its duration. Examples: `transition-timing-function: ease-in;`
- `transition-delay` Defines how long to wait between the time a property is changed and the transition actually begins. Examples: `transition-delay: 3s;`

Not all of these are required to build a transition, with the first three are the most popular.

# CSS Animations
Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.

There are three key advantages to CSS animations over traditional script-driven animation techniques:

1. They're easy to use for simple animations; you can create them without even having to know JavaScript.
2. The animations run well, even under moderate system load. Simple animations can often perform poorly in JavaScript.
3. Letting the browser control the animation sequence lets the browser optimize performance and efficiency.

## Setting Up An Animation
CSS animations are made up of two basic building blocks.

- Keyframes: define the stages and styles of the animation. Think of `@keyframes` as being stages along a timeline. 
- Animation Properties: assign the `@keyframes` to a specific CSS element and define how it is animated.


### The @keyframes
Here we'll set the animation stages. Our `@keyframes` properties are:

- A name of our choosing (demoFade in this case).
- Stages: 0%-100%; from (equal to 0%) and to (equal to 100%).
- CSS styles: the style that you would like to apply for each stage.
For example:

```css
@keyframes demoFade {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}
```
or
```css
@keyframes demoFade {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
```

<br>
### The Animation
The animation property is used to call `@keyframes` inside a CSS selector. 

Animation can have multiple properties:
- `animation-name`: @keyframes name (remember we chose tutsFade).
- `animation-duration`: the timeframe length, the total duration of the animation from start to the end.
- `animation-timing-function`: sets the animation speed ( linear | ease | ease-in | ease-out | ease-in-out | cubic-bezier ).
- `animation-delay`: the delay before our animation will start.
- `animation-iteration-count`: how many times it will iterate through animation.
- `animation-direction`: gives you the ability to change the loop direction, from start to end, or from end to start, or both.
- `animation-fill-mode`: specifies which styles will be applied to the element when our animation is finished ( none | forwards | backwards | both )

```css
.element {
  animation-name: demoFade;
  animation-duration: 4s;
  animation-delay: 1s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-direction: alternate;
}
```

<p data-height="207" data-theme-id="0" data-slug-hash="oLydYk" data-default-tab="result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/oLydYk/">Basic CSS Animation</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<br>
### Another Example from square to circle
<p data-height="425" data-theme-id="0" data-slug-hash="yJEjgd" data-default-tab="css,result" data-user="lexinamer" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/yJEjgd/">Basic CSS Animation- Circle to Round</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<br>

# Vendor Prefixes
CSS vendor prefixes, also known as or CSS browser prefixes, are a way for browser makers to add support for new CSS features before those features are fully supported in all browsers. 

From the perspective of a front-end web developer, browser prefixes are used to add new CSS features onto a site while still having comfort knowing that the browsers will support those styles. This can be especially helpful when different browser manufacturers implement properties in slightly different ways or with a different syntax.

Here are the current vendor prefixes but you should always check with the [MDN](https://developer.mozilla.org/en-US/docs/Glossary/Vendor_Prefix) guide to make sure its updated. 

- -webkit- (Chrome, Safari, newer versions of Opera.)
- -moz- (Firefox)
- -o- (Old versions of Opera)
- -ms- (Internet Explorer)

### How We Use
In most cases, to use a more advanced CSS style property such as animations or transitions, you take the standard CSS property and add the prefix for each browser. The prefixed verisons comes first (in any order you prefer) while the normal CSS property will come last. 

For example, if you want to add a CSS3 transition to your document, you would use the transition property as shown below:

```css
-webkit-transition: all 4s ease;
-moz-transition: all 4s ease;
transition: all 4s ease;
```

<br>
- Using Sass for Vendor Prefixes: https://www.himpfen.com/vendor-prefix-sass-mixin/
- All about vendor prefixes: http://webdesign.about.com/od/css/a/css-vendor-prefixes.htm
- Can you use the element: http://caniuse.com/
- Auto-parse your vendor prefixes: https://github.com/postcss/autoprefixer
