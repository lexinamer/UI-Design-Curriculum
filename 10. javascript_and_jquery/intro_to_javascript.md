---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4MiwiY29udGVudF90eXBlIjoiTGVzc29uIn0.kWe6blXWfK4xgByyEO34sQM5nWDcgy5oR9UejmlUVCI

title: >-
  Intro to Javascript
description: >-
  Javascript fundmanetals and introduction
---
# What is Javascript? 
JavaScript is a client-side programming language that adds interactivity and behavior to web pages. There are two ways to use javascript. When it is written to run in a browser it is often called "front-end" programming, and server-side JavaScript is usually considered "back-end" programming. Hint: It's not the same thing as Java.

![java](https://qph.ec.quoracdn.net/main-qimg-504a26ed8b7cefd1f29b992db733f592-c?convert_to_webp=true)
<br>

# How to set it up?
Similar to CSS, there are two ways. First, you can add it directly to your HTML Page.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Test Page</title>
    </head>
    <body>
    <p>This is my awesome JavaScript code.</p>
        <script>
            alert('Hello World!');
        </script>
    </body>
</html>
```

Second, you can add an external Javascript file. However, while you add a CSS file in the `<head></head>` tags you typically add a Javascript file at the bottom of the page before the closing `</body>`

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Test Page</title>
    </head>
    <body>
    <p>This is my awesome JavaScript code.</p>

     <script src="path/to/file.js"></script>
    </body>
</html>
```

# Syntax of Javascript

After each individual statement, you must add a semicolon. This helps the language determine where one statement ends and another begins. Semicolons can be a deep topic of discussion, but we'll keep things simple for you: end every line with a semicolon, unless we specifically ask you not to. Semicolons aren't always necessary, but they're a good habit for people new to JS, so we'll use them in this tutorial.

```
console.log('Hello World!');
console.log('I am glad to meet you');
console.log('I am fuzzy');
```

camelCase is popular in Javascript as it is what the originators of JavaScript decided to go with. However, more important than following an exact rule is the readability of your code.
```
var myName
var myAge
var myHometown
```

The Console lets you use standard JavaScript statements and Console-specific commands while a page is live in the browser to help you debug the page. We will use the one built into the Chrome dev tools.
![console](http://www.ikrazzy.com/wp-content/uploads/2012/02/chrome-javascript-error.jpg)


# Getting Javascript to the screen
There are numerous ways to get JS onto the screen. There are three common ones that we will use

Open a popup box.

```
alert('Hello World!');
```
				
Display a message in your console.

```
console.log('Hello World!');
````
				
Add something to the page.

```
document.write('Hello World!');
```
