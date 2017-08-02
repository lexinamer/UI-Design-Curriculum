---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4NCwiY29udGVudF90eXBlIjoiTGVzc29uIn0.RlcI0RxYjF8zW-VjLOdBSsnI60G1RfCkn0NgvKcgMnQ

title: >-
  Data and Operations
description: >-
  A programming language's primary features revolve around modeling a scenario and performing basic mathematical operations.
---
# Data and Types
JavaScript controls the behavior of the browser. Almost every interaction involves some kind of data. Whether it's text when updating your bio on social media, the number of cupcakes you'd like to order, or a "Yes, send me email updates" checkbox, there's generally some important information that needs to be acted upon. 

# Primative Data Types
JavaScript supports many types of data and each has its own unique meaning and syntax. _Primitive data types_ are those that are fundamental to storing the simplest data, like numbers and letters. The following table shows some of the primitive data types available in the JavaScript language.

Type | Syntax
:--- | :---
Number | `1`, `200`, `3.14159`
String | `"hello there!"`, `'hello there!'`
Boolean | `true`, `false`
Undefined | `undefined`

# Numbers
Numbers are represented exactly the way that you might expect: as numeric digits. The mathematical operators that you learned in school work on numbers (+, -, *, /). 

```javascript
// a number
1 

// another number, with decimal places
3.14159 

// this operation results in the number '10'
3 + 7 
```

Javascript can do basic math!

```javascript runnable
//addition and subtraction
console.log(3 + 4);
console.log(2 - 1);

//multiplication
console.log(4 * 8);

//division
console.log(2 / 7);
```

# Numbers and Order of Operations

![pemdas.jpg](https://tiy-learn-content.s3.amazonaws.com/b5c4b7c5-pemdas.jpg)

The order of operations will matter for calculations - so if you need to execute one operation before another, you should wrap parentheses around it (e.g. `(4 + 5) * 3`). Operations will be performed in the order of "Parentheses, Exponents, Multiplication, Division, Addition, Subtraction". It can be helpful to remember this order with the phrase "Please Excuse My Dear Aunt Sally" - both share the acronym **PEMDAS**. 

Let's see how wrapping parentheses around different pieces affects one equation:

```js
console.log(4.11 * 5.93 + -1 / 16);     // 24.3098
console.log(4.11 * 5.93 + (-1 / 16));   // 24.3098
console.log(4.11 * (5.93 + -1) / 16);   // 1.26639375
```


# Strings
As we've already seen, strings are data types that store words and characters. *To define a string, the words and characters need to be wrapped in single (') or double quotes (")*. Wrapping strings is important because it allows JavaScript to distinguish the string data type from an arbitrary JavaScript command.

```js
// A string can be any sequence of characters
"hello world" 

// This is also a string, but using single quotes
'I am also a string' 

// If you need to use the same kind of quote inside your string,
// use the backslash `\` to "escape" it
'It\'s great'

// ...or use another kind of quote to wrap it
"It's great"

// Here's a tricky one. This isn't a number.
// It's a string, because it's wrapped in quotes
"3" 

// This, however, is actually a number
3

// This is NOT a string! Notice the lack of quotes.
// JavaScript thinks this line is a variable called `thing`
thing 
```

# Concatenation
The `+` operator also works on strings and allows us to combine multiple strings into one. Combining strings is called **concatenation** and is incredibly common in programming.

```js runnable
// Add numbers with the `+` operator
console.log(2 + 10);

// Concatenate strings using the same operator
console.log("bubble" + "gum");

// Don't forget to include spaces to separate words
console.log("hello " + "world");

// Something curious will happen if you add a number to a string
console.log(3 + "3");
console.log("Windows" + 95);
```
