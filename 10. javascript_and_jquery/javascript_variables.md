---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4MywiY29udGVudF90eXBlIjoiTGVzc29uIn0.Qqp7mlEvlGy9eOopZ0yaGBJ5CJMKJ_YYsO5doqLWG24

title: >-
  Javascript Variables
description: >-
  Introduction to JS variables
---
# Variables
Variables are named "buckets" that hold data and make that data available for reuse later. A variable can hold data of any type, but for now we'll demonstrate them using a string. A string is a combination of letters, numbers, and special characters, surrounded by matching quote marks, which we will talk about later.

# Why Use Variables
Before we use a variable, let's look at a few strings. If strings aren't stored in variables, they have to be retyped later when you want to use that same string. This can result in a lot of duplication.

```
console.log("this is a string, but you can't reuse this.");
console.log("if you wanted to print the same text again later...");
console.log("you'd need to type it again...");
console.log("and again...");
console.log("and again...");
console.log("and again...");
```

If we store a string in a variable named sentence, we can reuse that variable.

```
var sentence = "if you store a string in a variable, it's easy to reuse.";

console.log(sentence);
console.log(sentence);
console.log(sentence);
```

# Declaring a Variable
To declare (create) a variable, just type the word "var" and the variable name. When you first create a variable, it does not have a value (it is undefined).

```
var numberOfCats;
```
				
It is a good idea to give your variable a starting value. This is called initializing the variable.

```
var numberOfCats = 5;
```

# Using a Variable
Once you have created a variable, you can use it in your code. Just type the name of the variable. Lets set up a JS practice directory to test this.

```
var numberOfCats = 5;
console.log(numberOfCats);
```


# Breaking it Down

![variable](https://tiy-learn-content.s3.amazonaws.com/9e2a068b-variables.jpg)

- `var` is a keyword in the JavaScript language. Keywords are words that have a particular meaning to the JavaScript language. When you write var you are telling JavaScript to create a variable. Be aware that var and "var" are different things to JavaScript. The first is a keyword that commands JavaScript to create a variable, while the second is just a string.

- `bucket` is the name that we are giving the variable. It's not a keyword; we can define any name that we want. We could have named the variable basket or shoe or thing. Unless it's a special reserved word, the specific name that you choose for a variable doesn't matter. It's up to you to decide a name that makes sense.

- `=` is the assignment operator. We'll discuss operators later in the crash course, but know that the assignment operator takes the value on its right and assigns it to the variable on its left. In the above code, = takes the string on the right and stores it in the newly created variable on the left.

- The semicolon `(;)` at the end of the line tells JavaScript that the statement is complete. A JavaScript statement is a single, complete instruction to be executed.
