# Functional Programming Concepts

### What is functional programming?

Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data. 

### What is a pure function and how do we know if something is a pure function?

* It returns the same result if given the same arguments (it is also referred as deterministic).
* It does not cause any observable side effects.

Imagine we want to implement a function that calculates the area of a circle. An impure function would receive radius as the parameter, and then calculate radius * radius PI:

``` js
let PI = 3.14;

const calculateArea = (radius) => radius * radius * PI;

calculateArea(10); // returns 314.0
```

Why is this an impure function? Simply because it uses a global object that was not passed as a parameter to the function.


### What are the benefits of a pure function?


**Reading Files**
If our function reads external files, it’s not a pure function — the file’s contents can change.

```js
onst charactersCounter = (text) => `Character count: ${text.length}`;

function analyzeFile(filename) {
  let fileContent = open(filename);
  return charactersCounter(fileContent);
}
```

**Random number generation**
Any function that relies on a random number generator cannot be pure.

```js
unction yearEndEvaluation() {
  if (Math.random() > 0.5) {
    return "You get a raise!";
  } else {
    return "Better luck next year!";
  }
}
```

### What is immutability?

When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
In Javascript we commonly use the for loop. This next for statement has some mutable variables.

```js

var values = [1, 2, 3, 4, 5];
var sumOfValues = 0;

for (var i = 0; i < values.length; i++) {
  sumOfValues += values[i];
}

sumOfValues // 15

```

For each iteration, we are changing the i and the sumOfValue state. But how do we handle mutability in iteration? Recursion!

```js
let list = [1, 2, 3, 4, 5];
let accumulator = 0;

function sum(list, accumulator) {
  if (list.length == 0) {
    return accumulator;
  }

  return sum(list.slice(1), accumulator + list[0]);
}

sum(list, accumulator); // 15
list; // [1, 2, 3, 4, 5]
accumulator; // 0
```

So here we have the sum function that receives a vector of numerical values. The function calls itself until we get the list empty (our recursion base case). For each "iteration" we will add the value to the total accumulator.
With recursion, we keep our variables immutable. The list and the accumulator variables are not changed. It keeps the same value.


### What is Referential transparency?

Let’s implement a square function:

```js
const square = (n) => n * n;
```

This pure function will always have the same output, given the same input.

```js
square(2); // 4
square(2); // 4
square(2); // 4
// ...
```

Passing 2 as a parameter of the square function will always returns 4. So now we can replace the square(2) with 4. That's it! Our function is referentially transparent.
Basically, if a function consistently yields the same result for the same input, it is referentially transparent.
**pure functions + immutable data = referential transparency**

---

# Nodejs

### What is a module?

A module is essentially another javascript file.

### What does the word ‘require’ do?

to use a functionality in another module we should require the name of the module that has the functionality.

### How do we bring another module into the file the we are working in?

Here we required a module named count in our current file

`require('./count');`


### What do we have to do to make a module available?

we need to export the module and chose what part we want to export.

for example in the count module we have a function called counter so we need to write:

`module.export = counter;`

and when we call that module we need to set this module to variable:

`let counter = require('/count');`