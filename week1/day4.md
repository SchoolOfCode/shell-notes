# Day 4

## Functions

```javascript
// define a function
function doCoolThing() {
  console.log("done cool thing!");
}

// call a function
doCoolThing(); // prints out "done cool thing!"
```

## Arrays and Objects

- same underneath - `{0:'a', 1:'b', 2:'c'}` is like `['a','b','c']`
- array has some differnet methods we will use soon.

## Functional Programming

- Why is functional programming good?

  - Small modules can be coded quickly and easily.
  - General purpose modules can be reusable, which leads to faster development of next programs.
  - The modules of a program can be tested independently, helping to reduce the time spent debugging.

- Callbacks

```JavaScript
var add = function(a, b, doSomething){
   doSomething(a+b)
}

add(1, 2, function(x){
  console.log(`the result is ${x}`)
})
//prints out "the result is 3"
```

- forEach

```javascript
var people = ["harry", "sat", "matt", "frances", "matt"];

function convertToUpperCase(string) {
  return string.toUpperCase();
}

people.forEach(convertToUpperCase);

// forEach visits each item in the array and mutates the array directly

console.log(people); // ["HARRY", "SAT", "MATT", "FRANCES", "MATT"]
```

- map

```javascript
var people = ["harry", "sat", "matt", "frances", "matt"];

function convertToUpperCase(string) {
  return string.toUpperCase();
}

var capitalisedPeople = people.map(convertToUpperCase);

// map returns an array which is stored in capitalisedPeople
console.log(people); //["harry", "sat", "matt", "frances", "matt"]
console.log(capitalisedPeople); // ["HARRY", "SAT", "MATT", "FRANCES", "MATT"]
```

- filter

```javascript
var people = ["harry", "sat", "matt", "frances", "matt"];

function isPersonNotCalledHarry(string) {
  return string !== "harry";
}

var peopleNotCalledHarry = people.filter(isPersonNotCalledHarry);

// filter returns array of all items for the callback function resolves to true
//peopleNotCalledHarry = ["sat", "matt", "frances", "matt"]
```

- reduce

```javascript
var numbers = [1, 2, 3, 4, 5];

function add(total, current) {
  return total + current;
}

var numbersTotal = numbers.reduce(add, 0);

console.log(numbersTotal); // 15
```

- forEach mutates original array, map, filter and reduce return new arrays.
- because they return an array you can call another method on whats returned

```javascript
var list = [1, 5, 6, 7, 2, 3, 4, 8, 9, 10];

function add1(num) {
  return num + 1;
}

function isGreaterThanFive(num) {
  return num < 5;
}

// here .filter() is called on the new array that .map() returns and the final result is stored in newList
var newList = list.map(add1).filter(isGreaterThanFive);
```

- Array Method Challenges
  1. Keep only the force users, and return a new array of their names
  2. Create a new array and into it -> If last name is "Skywalker", their shooting score add 10, else their shooting score minus 10

```javascript
var personnel = [
  {
    id: 5,
    name: "Luke Skywalker",
    pilotingScore: 98,
    shootingScore: 56,
    isForceUser: true
  },
  {
    id: 82,
    name: "Sabine Wren",
    pilotingScore: 73,
    shootingScore: 99,
    isForceUser: false
  },
  {
    id: 22,
    name: "Zeb Orellios",
    pilotingScore: 20,
    shootingScore: 59,
    isForceUser: false
  },
  {
    id: 15,
    name: "Ezra Bridger",
    pilotingScore: 43,
    shootingScore: 67,
    isForceUser: true
  },
  {
    id: 11,
    name: "Caleb Dume",
    pilotingScore: 71,
    shootingScore: 85,
    isForceUser: true
  }
];
```

## Default Parameters

```javascript
// instead of
function getFullName(firstName, lastName) {
  if (typeof firstName === "undefined") {
    firstName = "first";
  }
  if (typeof lastName === "undefined") {
    firstName = "last";
  }
  return firstName + " " + lastName;
}

// you can give default parameters like this

function getFullName(firstName = "first", lastName = "last") {
  return firstName + " " + lastName;
}
```

## String Methods

- `.split()` example

```javascript
var name = "christiano ronaldo";

name.split(" "); // ["christiano", "ronaldo"]
name.split("iano ronal"); // ["chris", "do"]
name.split(""); // ["c","h","r","i","s","t","i","a","n","o"," ","r","o","n","a","l","d","o"]
```

- [More String Methods](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Useful_string_methods)

## Spread Operator `...`

- with arrays

```javascript
var array = [1, 2, 3, 4, 5];

var newArray = [...array, 6, 7, 8];

console.log(newArray); // [1,2,3,4,5,6,7,8]
```

- with objects

```javascript
var luke = {
  id: 5,
  name: "Luke Skywalker",
  pilotingScore: 98,
  shootingScore: 56,
  isForceUser: true
};

var newLuke = {
  ...luke, // spreads out all of luke properties into newLuke
  pet: "cat" // adds pet property
};

newLuke.id === 5; // true
newLuke.pet === "cat"; // true
```

## Variables into Objects

- Variable's name become the key
- Variable's value becomes value
- Example:

```javascript
var name = "Luke Skywalker";
var isForcerUser = true;

var luke = {
  name,
  isForceUser
};

console.log(luke); // {name: "Luke Skywalker", isForceUser: true}

// it is the same as:
var luke = {
  name: name,
  isForceUser: isForceUser
};
```

## Code Wars

- Sign up and start training!
- [codewars.com](https://www.codewars.com/);

## DOM (document object model)

- When a web page is loaded, the browser creates a Document Object Model of the page.
- The HTML DOM model is constructed as a tree of Objects

```html
<html>
  <head>
    <title>DOM DOM DOM</title>
  </head>
  <body>
    <h1>Welcome!</h1>
    <p>lets learn about the DOM</p>
  </body>
</html>
```

the modal of the html would look something like this`*`:

```javascript
var document = {
  head: {
    title: "DOM DOM DOM"
  },
  body: {
    h1: "Welcome!",
    p: "lets learn about the DOM"
  }
};
```

`*` slightly oversimplified but you get the idea

### Accesing the DOM with JavaScript

- here we have an unordered list with several list items:

```html
<ul id="list">
  <li class="listItem">dogs</li>
  <li class="listItem">cats</li>
  <li class="listItem">frog</li>
  <li class="listItem">rats</li>
  <li class="listItem">fish</li>
</ul>
```

- this is our JavaScript:

```javascript
var list = document.getElementById("list"); //  returns the element with an id of "list"

var listItems = document.getElementsByClassName("listItem"); // returns a node list of things with a class of "listItem"
```

- [All HTML Element Properties](https://www.w3schools.com/jsref/dom_obj_all.asp)

### Calling a function onclick

```html
<button onclick="doThing()">click to do thing</button>
```

```javascript
// button will call this function when clicked
function doThing() {
  console.log("done thing");
}
```

- [onclick attribute](https://www.w3schools.com/tags/ev_onclick.asp)

## Use DOM manipulation to bring Rock/Paper/Scissors to life

- instead of printing the result to the console
- use DOM manipulation to display it on the page
- call functions with onclick attribute for interactivity
