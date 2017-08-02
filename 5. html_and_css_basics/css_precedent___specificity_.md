---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE1OCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.WxD7VyE6PEL3nxFLPG42YjOZsfBrDMcJgHX3r3GDadk

title: >-
  CSS Precedent / Specificity 
description: >-
  When you have two competing css rules, who wins?
  Competing rules are two rules that should be styling the same elements, but have conflicting styles.
   
---
## Rule 1) Order. _(Last one wins)_
If you have two rules, the lower of the two will win, because it came last. This is part of the cascading, in CSS.

**The order determines the winner only if there are no other rules in play.**
 
 ```css
 .bar {
   color: red;
 }
 
 .bar {
   color: blue; /* ! winner ! */
 }
 ```
 
## Rule 2) Element(s)
Targeting an element is the most basic way of styling an element on the page. By default, these will always be determined by order unless you select more than 1 element, to increase the specificity.

<p data-height="268" data-theme-id="22603" data-slug-hash="reVbev" data-default-tab="result" data-user="jah2488" class="codepen">See the Pen <a href="http://codepen.io/jah2488/pen/reVbev/">reVbev</a> by Justin Herrick (<a href="http://codepen.io/jah2488">@jah2488</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

## Rule 3) Class(es)
Targeting a class in your css is our go-to way of styling our page. Targeting a class will override any styles that are only using element selectors. Using multiple classes will increases the specificity of the selector.

<p data-height="268" data-theme-id="22603" data-slug-hash="NNqmGb" data-default-tab="result" data-user="jah2488" class="codepen">See the Pen <a href="http://codepen.io/jah2488/pen/NNqmGb/">NNqmGb</a> by Justin Herrick (<a href="http://codepen.io/jah2488">@jah2488</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

## Rule 4) IDs
Applying a style to an ID (`#main-header`), will beat all above rules as it is more specific. This is why we highly discourage styling IDs. 

<p data-height="268" data-theme-id="0" data-slug-hash="LNVawM" data-default-tab="result" data-user="jah2488" class="codepen">See the Pen <a href="http://codepen.io/jah2488/pen/LNVawM/">LNVawM</a> by Justin Herrick (<a href="http://codepen.io/jah2488">@jah2488</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


## Rule 5) (inline) style
Any style defined directly on the HTML element will override *any* styles defined in the CSS. We want to avoid this at all costs. It leads to main painful sessions of trying to get your css files to work correctly.

```html
  <div id='my-container'>
    <div class='home'>
      <a href='#foo' style="color: red;">Hahah I win!</a>
    </div>
  </div>
```
```css
  #my-container .home a {
    color: blue; /* I lose */
  }
```

![https://css-tricks.com/wp-content/csstricks-uploads/specificity-calculationbase.png](https://css-tricks.com/wp-content/csstricks-uploads/specificity-calculationbase.png)

## Setting up a CSS Page
Here is one recommended way to start thinking about all of this! Think broad and then go more specific.
