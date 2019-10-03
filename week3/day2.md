# Day 2

## TDD Codewars

## DOM recap tasks

## REST APIs

- `put` vs `patch`
- `post`
- `get`
- `delete`
- restful design

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.use(express.json()); // parses body

// GET all users
app.get("/users", (req, res) => {
  // logic here
  res.send(`all users`);
});

// GET specific user
app.get("/users/:id", (req, res) => {
  const { id } = req.params;
  // logic here
  res.send(`user with id ${id}`);
});

// POST a new user
app.post("/users", (req, res) => {
  const newUser = req.body;
  // logic here
  res.send(`created user called ${newUser.name}`);
});

// PATCH a user
app.post("/users/:id", (req, res) => {
  const { id } = req.params;
  const userUpdates = req.body;
  // logic here
  res.send(`updated user with id ${id}`);
});

app.listen(port, () => console.log(`listening on port ${port}!`));
```

## Pokedex

- file system
- post pokemon

[home](../README.md)
