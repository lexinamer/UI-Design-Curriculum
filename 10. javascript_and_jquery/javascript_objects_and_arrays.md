---
# This section is used to set the title and description of the lesson on Newline. Do not edit `token`.
# Changes you make here will overwrite the existing content on Newline when synced via Github.
# Begin the body of the lesson below the final `---`.

token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJjb250ZW50X2lkIjoyMjE4NSwiY29udGVudF90eXBlIjoiTGVzc29uIn0.YPwR8TmD511mFXg6fuW5lJl8L4WuJOZ-mZiqaBcYT9g

title: >-
  Javascript Objects and Arrays
description: >-
  Keeping data contained and well-organized would be a challenge without ways to structure data. Fortunately Javascript has two very popular mechanisms for this: objects and arrays.
---
# What are they?
Often in programming, a need arises to represent some complex thing or idea in data. Objects and arrays allow us to do just that by grouping together like items that we can call over and over. Think of it as a complex variable. 

For example, this approach would quickly because infeasible especially if we have multiple dogs. You can restructure this code using objects and arrays to make it much easier to deal with.

```
var dogName = "Fluffy";
var dogAge = 8;
var dogColor = "brown"
```

# Objects 
Javascript objects are composed of a bunch of different properties, each of which has a different value. This is similar to how we often think of objects in real life; for example, a car may have a color (red, blue, silver, etc), number of tires, a make, a model, and a year of manufacture. The way we'd represent that in Javascript is:

```
var myCar = {
   color: "red",  // the 'color' property is a string
   numTires: 4,   // the 'numTires' property is a number
   make: "Hyundai",
   model: "Sonata",
   year: 2007
};
```

Objects can have any number of properties, and properties can contain any type of data (including other objects!). In the case of our dogs described above, we can simplify the code somewhat:

```
var dog1 = {
   name: "Fluffy",
   age: 8,
   color: "brown",
   description: {
        hair: "long",
        coat: "fluffy"
     }
};

var dog2 = {
   name: "Patches",
   age: 3,
   color: "black",
   description: {
        hair: "short",
        coat: "coarse"  
     }
};


// You can now use dot notation to reference the individual elements:
//   dog1.name
//   dog2.description.hair
```

In addition to using the "dot syntax" to access properties on an object (like dog1.name) you can also use the square bracket syntax: dog1["name"] . This syntax may look more verbose, but because the property name is a string now, we can compose it, or use an expression to determine it. 

While this doesn't necessarily shorten the length of our code, it can help structure information better. Nevertheless, we've still got problems with our code because we can't support an arbitrary number of dogs, and it's still hard to perform operations across all dogs like listing them in a display of some kind. Arrays will help with that.


# Arrays
An array is a "collection", a data structure used to keep track of multiple values. In some ways they're similar to objects without the named properties. Arrays are often (but not always) used for creating groups of similar items.

```
// Three different arrays; some containing the same type of data and some not.

var favoriteNumbers = [5, 6, 100];

var thingsILike = [5, 6, 100, "running", "cats", dog1]; // dog1 from the Objects section

var dogs = [dog1, dog2]; // these are the two variables from the objects above
```

Arrays can contain any number of items and can also be modified while the program is running. Arrays (a type of object) have methods (something that provides functionality related to objects) associated with them that provide a bunch of common operations that you might want to do on a list of things, such as finding the length, extracting a particular item in the list, or sorting the list. 

Arrays are zero-indexed, which means each position in the array has a number, starting with zero on the far left and counting up from there.

![arrays](https://tiy-learn-content.s3.amazonaws.com/2f957762-js-arrayindex.png)

```
var favoriteNumbers = [5, 6, 100];

favoriteNumbers[0] // Get the first element of the array
favoriteNumbers[2] // Get the third (last) element of the array

favoriteNumbers.push(8) // This is a method (note the parentheses at the end). It will add the number 8 to the favoriteNumbers array. 

favoriteNumbers.length // Get the length of the array. Note that this is a field, not a method.

favoriteNumbers.sort() // Sorts the list in increasing order (though that's customizable).
```

# Useful Methods
There are a bunch of built-in methods that are available on arrays. The full list is [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), but understanding adding ([push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push)), removing ([pop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop), [shift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift), [splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)), finding individual elements (`[]` operator), and finding the length ([length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/length)) will be a strong start.

Looking back at our dogs, we can further improve our code by getting rid of individual dog variables and instead putting them in an array:

```
// Note the difference between the square and curly braces. The square braces indicate the start and end of the array, and the curly braces indicate the start and end of objects.

// This array contains two different objects.

var dogs = [{
   name: "Fluffy",
   age: 8,
   color: "brown",
   description: {
        hair: long,
        coat: fluffy  
        }
  },
   {
   name: "Patches",
   age: 3,
   color: "black",
   description: {
        hair: short,
        coat: coarse  
        }
  }
];

dogs.length // returns: 2
dog[0].name // returns: "Fluffy"
dogs[1].name // returns: "Patches"
```
