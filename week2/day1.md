|[home](../README.md)|

# Day 3

## Event Listeners

```javascript
var button = document.getElementById("button");

button.addEventLister("click", myFunction);

function myFunction() {
  // whatever is is you want to do on click
}
```

- [Event Listeners](https://www.w3schools.com/js/js_htmldom_eventlistener.asp)
- [All HTML DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp)

### Adding Classes to Elements

```javascript
var myDiv = document.getElementById("my-div");

myDiv.classList.add("new-class"); // adds class
myDiv.classList.contains("new-class"); // returns true/false
myDiv.classList.remove("new-class"); // removes class
myDiv.classList.toggle("new-class"); // adds/removes class if not there or there
```

```css
.new-class {
  /* whatever you want to add */
}
```

- [classList refernce](https://www.w3schools.com/jsref/prop_element_classlist.asp)

## HTML/CSS House Challege

[Instructions](https://github.com/CodeYourFuture/build-a-house)

## Responsive Design

- vw, vh, %,flex
- @media rule

```css
/* this will only be applied when the screen is under 600px */
@media only screen and (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

## Error Handling

- any error thrown in the try block will be cought by the catch block
- finally block runs in either case
- throw new Error allows you to throw your own custom errors

```javascript
var data = { name: "ben" };

try {
  if (!data.age) {
    throw new Error("missing data");
  }
  console.log("the age was" + data.age);
} catch (err) {
  console.log(err);
} finally {
  console.log("i run error or no error");
}
console.log("i run afterwards");
```

## Scope

- var/let/const
- [function/block/global scope](https://www.w3schools.com/jS/js_let.asp)

## JS Quirks

- [truthy/falsy](https://www.sitepoint.com/javascript-truthy-falsy/)
- [pizza cutter analogy](https://www.quora.com/Why-is-0-1+0-2-not-equal-to-0-3-in-most-programming-languages)
- All values are truthy unless they are defined as falsy
  - false
  - 0
  - ""
  - null
  - undefined
  - NaN
