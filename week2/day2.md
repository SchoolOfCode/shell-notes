|[home](../README.md)|

# Day 2

## CodeWars

- remember to plan with pseudo-code.

## SetTimeout

```javascript
console.log("A");

setTimeout(() => {
  console.log("B");
}, 2000);

console.log("C");
// prints "A" then "C" then 2000ms later prints "B"

// Loops w/setTimeout
for (var i = 0; i < 10; i++) {
  setTimeout(() => {
    console.log(i);
  }, 2000);
}

for (let i = 0; i < 10; i++) {
  setTimeout(() => {
    console.log(i);
  }, 2000);
}

// the for loop with var will print out 10 ten times.
// the for loop with let will print out 0 - 9.
// this is because each let is scoped to the block as the for loop runs.
```

### Challenge

- print out a word letter by letter using setTimeout.

## Explaination of Async, Callbacks, and the Event Loop

- [video](youtube.com/watch?v=8aGhZQkoFbQ)

## Fetch

```javascript
// with .then()
fetch("https://icanhazdadjoke.com/", {
  headers: { Accept: "application/json" }
})
  .then(res => res.json())
  .then(data => console.log(data));

// with async/await
async function getDadJoke() {
  const result = await fetch("https://icanhazdadjoke.com/", {
    headers: { Accept: "application/json" }
  });

  const data = await result.json();
  console.log(data.joke);
}

getDadJoke();

// async/await with try/catch
async function getErrorProofDadJoke() {
  try {
    const result = await fetch("https://icanhazdadjoke.com/", {
      headers: { Accept: "application/json" }
    });

    const data = await result.json();
    console.log(data.joke);
  } catch (err) {
    console.log(err);
  }
}

getErrorProofDadJoke();

// how promises work (ish)
function resolveAfter2Seconds() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve("resolved");
    }, 2000);
  });
}

async function asyncCall() {
  console.log("calling");
  var result = await resolveAfter2Seconds();
  console.log(result);
  // expected output: 'resolved'
}

asyncCall();
```

### JavaScript 30

- [javascript30.com](https://javascript30.com/)
