---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4OSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.ksj_2GLJRriNijFNMdQs226OTHfjo4AORv7PTUplmjE

title: >-
  Javascript Loops
description: >-
  Round and round and round we go!
---
# Loops
Javascript loops are a way of repeating sections of code over and over, so that you're not having to re-write code again and again manually. For as long as a specified condition is true, the loop will continue to execute your code. There are many types of loops with these being the most common.

`while`: loops through a block of code while a specified condition is true. 

`for`: loops through a block of code a specific number of times


# While Loops
While loops repeat the same code over and over until a predefined condition is satisfied. If the condition statement is always true, then you will never exit the while loop and crash the browser, so be very careful when using while loops!

```
while (variable |operator| endvalue) {
    // do something
} 
```

## Age Example - While Loop

```
// This is a variable age and a basic while loop

var age = 5; 

while (age < 10) {
   console.log("You are younger than 10!");
}

document.write("You are over 10!");
```

This is saying the age is 5 which is less than 10, so the conditional is true. The loops will run over and over until the conditional becomes false. 

This will crash the computer. So we need to somehow set the age at some point to become over 10 to break out of the loop.

```js
// Lets add an increment operator that will add 1 to the age every time this while loop runs 

var age = 5; 

while (age < 10) {
   console.log("You are younger than 10!");
   age++;
}

document.write("You are over 10!");
```


# For Loops
An easier way to iterate through a loop is via the `for` loop. A `for` loop does exactly the same thing as a while loop, but it has the advantage of organizing it's components more locally and neater. It runs over and over until you declare a change in the statement so that it knows when to stop.

```js
for (variable |operator| initial; variable |operator| conditional; increment) {
    // do something
}
```

## Age Example- For Loop

```
// This is a variable age and a basic for loop

for (age = 5; age < 10; age++ ) {
   console.log("You are younger than 10!");
}

document.write("You are over 10!");
```


## Using an Array and For Loop 
```
var cats = ["fluffy", "zoey", "rue", "patches", "chomper"];

for (i = 0; i < cats.length; i++) {
  console.log("This is cat " + i);
}

document.write("All cats here!");
```

The 4 important aspects of a `for` loop:
1. **Initial variable:** usually used only in the `for` loop to count how many times the for loop has looped. `i` is a default variable for index. 
2. **The conditional statement:** It is what decides whether the for loop continues executing or not. 
3. **Increment or counter variable:** This tells us in what increment we want to run through the loop. Typically `i++` for adding 1.
4. The code that is executed for each loop. In this, its `console.log();`


# Practice Problem
Create a loop to count from 0-10.


# Breaks and Continues
The break statement "jumps out" of a loop while the continue statement "jumps over" one iteration defined in the loop.

```
// Break Statement
var i;
for (i = 0; i < 10; i++) {
    if (i === 3) { break; }
    document.write("The number is " + i + "<br>");
}

// Continue Statement (
var i;
for (i = 0; i < 10; i++) {
    if (i === 3) { continue; }
    document.write("The number is " + i + "<br>");
}
```


