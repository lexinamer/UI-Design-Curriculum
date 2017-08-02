---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE3NiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.CEsObV45x3YFLKPs_HWsZQbyD8dTENZzZlJGfRIkTCU

title: >-
  Basics of Sass 
description: >-
  Enhance your CSS through Sass
---
# Sass
Sass is a preprocessor for CSS. Sass adds a lot of useful features on top of CSS that make our lives as web developers and designers easier.

## A Few Things Before We Start
- All Sass files end with `.scss`, this is how we know its a sass file.
- The browser __cannot__ read a Sass (`.scss`) file, so we need to transform our `.scss` files into `.css` files. 
- You can write all regular `css` in a sass file.
- You __cannot__ write sass in a `css` file.


# How It Works
1. Install the Sass gem via the command line [here](http://sass-lang.com/install)
2. In our HTML we **still** link to our main `.css` file, as we did before.
3. In the command line, you must use `sass --watch FOLDER_TO_WATCH` we can have sass _automatically_ compile our `scss` files into `css` files every time we change the `scss` file. This allows us to just save our `scss` file and go reload the browser immediately.
4. Be sure to not add any code or styles to your `.css` files when using sass, because every time sass _recompiles_ it will **erase** everything in your `.css` files and replace it with new `.css`. 

## Nesting
- Browsers cannot understand a nested style, but sass will allow us to write our styles nested, to save us typing and time.

```scss
header {
  background: blue;
  nav {
    background: white;
  }
}
```
compiles to:

```css
header {
  background: blue;
}
header nav {
  background: white;
}
```

Sass can help us clean up our code by writing this:

```scss
ul {
  background-color: #666;
  li {
    background-color: pink;
    a {
      color: red;
    }
  }
}
```

instead of

```css
ul {
  background-color: #666;
}

ul li {
  background-color: pink;
}

ul li a {
  color:red;
}
```

## Variables
Its hard to remember which color is being used where when everything is just a #477CSD code. Its also a pain to change those colors everywhere in the code when the design changes. Sass variables allows us to reuse that value everywhere in our scss. Variables must appear above the point where they are being called.  If they aren't the browser won't be able to recognize what the value is supposed to be.

```scss
  $primary-color: #A237FF;
  $secondary-color: #2BC4F2;
  
  header {
    background: $secondary-color;
    color: $primary-color
  }
  
  nav a:hover {
    color: $secondary-color;
  }
  
  .my-button {
    background-color: $primary-color;
    border-color: $secondary-color;
  }
```

turns into valid css:

```css
  
  header {
    background: #2BC4F2; 
    color: #A237FF;
  }
  
  nav a:hover {
    color: #2BC4F2;
  }
  
  .my-button {
    background-color: #A237FF;
    border-color: #2BC4F2;
  }
```

You can use variables to hold any value 

```scss
  $header-size: 4em;
  
  h1 {
    font-size: $header-size;
  }
```

``` css

  h1 {
    font-size: 4em;
  }

```

## Mixins
Some things in CSS are a bit tedious to write over and over. A mixin lets you make groups of CSS declarations that you want to reuse throughout your site. You can even pass in values to make your mixin more flexible. A good use of a mixin is for vendor prefixes. Here's an example for vertical centering. 

``` scss
  @mixin verticalcenter {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
  }
  
  h1, h2, h3 {
    @include verticalcenter;
  }
```
compiles to:

```css
  h1 {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
  }

  h2 {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
  }

  h3 {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
  }
```

## Partials
To prevent our `scss` from becoming one giant file that is hard to manage and read, Sass allows us to break up our code into multiple files and then `@import` them into our main `scss` file.

- All files you want to create to be imported must start with an `_` (underscore). We refer to these as "partials", because they are a piece of the entire scss. So if I wanted to keep all my variables in their own file, it would be called something like `_variables.scss`
- You import a file by saying `@import NAME_OF_PARTIAL`

```scss
  // This is my _variables.scss
  
  $primary-color: #333;
```

```scss
  // This is my main.scss
  
  @import "variables"; // Notice there is no underscore or .scss
  
  nav {
    color: $primary-color;
  }
```
compiles to:

```css
  nav {
    color: #333;
  }
```

## Extends
This is one of the most useful features of Sass. Using `@extend` lets you share a set of CSS properties from one selector to another. It helps keep your Sass very DRY. In our example we're going to create a simple series of messaging for errors, warnings and successes. http://codepen.io/lexinamer/pen/wWjRQL

``` scss
.message {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.success {
  @extend .message;
  border-color: green;
}

.error {
  @extend .message;
  border-color: red;
}

.warning {
  @extend .message;
  border-color: orange;
}
```
compiles to:

```css
.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```

## More Sass Goodness!!
http://sass-lang.com/guide

