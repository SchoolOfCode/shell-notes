# Day 3

## Recap for Matt

- node
- testing
- jest
- classes
- canvas
- css variable
- joke website
- express
- rest APIs
- crud
- destructuring
- ternary operator
- dom recap tasks
- CRUD operations
- pokedex

## CRUD on the Pokedex

- filesystem
- async/await

## Callbacks, Promises and async/await

```javascript
withCallBack();
withPromise();
withAwait();

function withCallBack() {
  makeMeWriteCallback(data => console.log(data), "callback");
}

function withPromise() {
  makeMeWait("promise").then(message => console.log(message));
}

async function withAwait() {
  const message = await makeMeWait("async/await");
  console.log(message);
}

function makeMeWriteCallback(cb, msg) {
  setTimeout(() => cb("You are calling me from a " + msg), 1000);
}

function makeMeWait(msg) {
  return new Promise((resolve, reject) => {
    makeMeWriteCallback(resolve, msg);
  });
}
```

## Fetch

### these two functions do the same thing

```javascript
// with .then()
function fetchMeTheStuff() {
  fetch(`<url>`)
    .then(response => response.json())
    .then(data => doSomething(data))
    .catch(err => console.log(err));
}

// with async/await
async function fetchMeTheStuff() {
  try {
    const response = await fetch(`<url>`);
    const data = await response.json();
    doSomething(data);
  } catch (err) {
    console.log(err);
  }
}
```

### Using fetch for more than get

```javascript
function postData() {
  const options = {
    method: "POST", // method defaults to GET. You can specify POST/PATCH/PUT/DELETE
    headers: { "Content-Type": "application/json" }, // telling the server we are sending a JSON string
    body: JSON.stringify(`<data>`) // sending the JSON string in the body
  };
  const result = await fetch(`<url>`, options);
  const data = await result.json()
  console.log(data)
}
```

[home](../README.md)
