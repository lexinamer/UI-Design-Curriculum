---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4OCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.L5pCPw-REr81c31u6BXpTiM0scy0cJGgROb3572w07c

title: >-
  If Statements
description: >-
  Using logic to help write Javascript functions
---
# If and If/Else Statements
These are conditional statements that are used to perform different actions based on different conditions. There are 3 main types of conditionals that we can use together to create logic. 

# If Statements
The if statement executes a statement if a specified condition is true. If the condition is false, another statement can be executed.

``` 
if (expression) {
  // if the expression is true, the code inside these brackets will run.
} 
```

# Else Statements
The if/else statement provides an alternate set of instructions in case the if statement is false.

```
if (expression) {
  // if the expression is true, the code inside these brackets will run
} else {
  // some other code will run
}
```

# Else If Statements
You can also add another option using `else if`

```
if (expression1) {
   // if true, do this
} else if (expression2) {
  // if false, do this
} else {
  // if both false, do this
}
```

# An example to see how this works: 
<p data-height="265" data-theme-id="0" data-slug-hash="RRYPxZ" data-default-tab="js" data-user="lexinamer" data-embed-version="2" data-pen-title="If/Else Test" class="codepen">See the Pen <a href="http://codepen.io/lexinamer/pen/RRYPxZ/">If/Else Test</a> by Lexi Namer (<a href="http://codepen.io/lexinamer">@lexinamer</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

# Practice Problem
1. Create a variable that gives a prompt asking for the temperature
2. Using if and else if statements, make it do the following: 
- If it is greater than 100, stay inside.
- If it is between 60 and 99, wear a t-shirt.
- Otherwise, use common sense.

