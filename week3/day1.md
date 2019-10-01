# Day 1

## TDD Codewars

- alphabet kata
- reduce recap
- findIndex(item => item.something === somethingElse)
- while loop

## API

### Express

- Express helps us easily make an enpoint available on a port of our choosing that will recieve and respond to HTTP requests

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.get("/myroute", (req, res) => {
  res.send("HELLO WORLD");
});

app.listen(port, () => console.log(`listening on port ${port}!`));
```

### REST APIs

- a convention for intuitive api design
- CRUD operations (create, read, update, delete)
- semantic HTTP verbs (`GET`, `POST`, `PATCH`/`PUT`, `DELETE`)
- a `GET` request to `/users` should get users
- a `GET` request to `/users/<user_id>` should get the one user with that id
- `POST` to `/user` should create a new user
- `PATCH` to `/user/<user_id>` should update some fields on a user
- `PUT` to `/user/<user_id>` should replace old user data with new user data
- `DELETE` to `user/<user_id>` should delete user with that id
- paramaters and query string (`params` and `query`)

## Pokedex API

- creating our own api that will get pokemon

## Destructuring

### With Objects

```javascript
const object = {
  name: "Henry",
  type: "hoover",
  settings: ["high", "low"],
  color: "red",
  priceGBP: 100
};

// instead of this:
const name = object.name;
const type = object.type;
const settings = object.settings;
const color = object.color;
const priceGBP = object.priceGBP;

// you can do this:
const { name, type, settings, color, priceGBP } = object;
```

### With Arrays

```javascript
const array = ["hoover", "dyson", "g-tech", "dust devil"];

// instead of this
const firstItem = array[0];
const secondItem = array[1];
const thirdItem = array[2];

// you can do this
const [firstItem, secondItem, thirdItem] = array;
```

### `...`

```javascript
const object = {
  type: "house",
  size: "big",
  hasRoof: true,
  isAffordable: false
};

const { type, ...rest } = object;

console.log(type); // "house"
console.log(rest); // { size: "big", hasRoof: true, isAffordable: false }

const array = [1, 2, 3, 4, 5];

const [firstItem, ...allOtherItems] = array;

console.log(firstItem); // 1
console.log(allOtheItems); // [2, 3, 4, 5]
```

## Ternary Operator

```javascript
console.log(1 < 4 ? "hello" : "goodbye"); // hello
console.log(1 > 4 ? "hello" : "goodbye"); // goodbye
```
