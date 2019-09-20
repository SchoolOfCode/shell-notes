# Day 3

### JavaScript Introduction

- cool video

### JS Basics

- Types:
  - string `"i'm a string"`
  - number `123`
  - boolean `false`/`true`
  - array `[1,2,3]`
  - object `{ firstName: "ben", lastName: "lee", age: 27 }`
  - null `null`
  - undefined `undefined`
- Variables -> `var myThing = "some thing"`
- Operators
  - assignment `=`, `+=`, `-=`, `++`, `--`
  - mathmatical `+`, `-`, `*`, `/`, `**`
  - equality `==`, `===`, `>`, `<`, `>=`, `<=`, `!=`, `!==`
  - logical `&&`, `||`

### Logic Flow

- if statements

```javascript
if (true) {
  //do something
}
if (false) {
  //don't do something
}
```

- else clauses

```javascript
if (true) {
  //do something
} else {
  //do this thing instead
}
```

- else if clauses

```javascript
if (true) {
  //do something
} else if (true) {
  //do this thing instead
} else {
  // do this thing
}
```

- switches

```javascript
switch (expression) {
  case value1:
    //Statements executed when the
    //result of expression matches value1
    break;
  case value2:
    //Statements executed when the
    //result of expression matches value2
    break;
  case valueN:
    //Statements executed when the
    //result of expression matches valueN
    break;
  default:
    //Statements executed when none of
    //the values match the value of the expression
    break;
}
```

### Rock, Paper, Scissors

- Use JavaScript to play RPS
- For now, write you js in a `<script></script>` tag
- Compare two choices and print the winner in console
- Use pseudo-code to plan what cases you need to check
- Convert that pseudo-code into JavaScript
- Next, generate a random computer move and allow player to input their move

### Functions

- what is a function
- DRY (don't repeat yourself)
- paramaters/arguments

```javascript
function returnThing(parameter1, parameter2) {
  return `${parameter1} ${parameter2}`;
}

var myThing = doThing("argument1", "argument2");

myThing === "argument1 argument2"; // true
```

- Pure Functions
  - a function that does not rely on external variables.
  - good principle to stick to for robust code.

### Loops

- while

```javascript
var i = 0;
// executes then loops only while condition resolves to true
while (i < 10) {
  text += "The number is " + i;
  i++;
}
```

- do while

```javascript
var i = 0;
// executes once whatever then loops while resolves to true
do {
  text += "The number is " + i;
  i++;
} while (i < 10);
```

- for

```javascript

for (statement 1; statement 2; statement 3) {
  // code block to be executed
}
// Statement 1 is executed (one time) before the execution of the code block.

// Statement 2 defines the condition for executing the code block.

// Statement 3 is executed (every time) after the code block has been executed.

// eg.

for (var i = 0; i < 10; i++) {
  text += "The number is " + i;
}
```

### Refactor RPS

- Cut out repetition by writing functions
- Write functions you can reuse
- Use a while loop to play game again
- Link external js file:

  ```html
  <script>
    // JavaScript code can go here
  </script>

  <!-- or you can link external file like so: -->
  <script src="main.js"></script>

  <!-- script tags should be the last thing in your body tag so that they run the script after the page has loaded -->
  `
  ```

### Code Review

- What did they do differently - why?
- What did they do the same - why?
- How could it be better?

### Quirks of JS

- truthy / falsey
- string + number
- funny memes

### Shell Energy Home Page

- Continue Recreating [Shell Energy Website](https://www.shellenergy.co.uk/)