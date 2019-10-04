|[home](../README.md)|

# Day 4

---

## Express Recap

[expressjs.com](https://expressjs.com/)

### Serving an html file with express

```javascript
const express = require("express");
const app = express();
const port = 3000;

const path = require("path");

app.get("/", (req, res) => {
  res.sendFile(path.join(__dirname, `<path_to_file>`));
});

app.listen(port, () => console.log(`listening on port ${port}!`));
```

### Making files available in public folder

Using `app.use(express.static())` in this way means the `<name_of_folder>` folder in your project folder can be accessed by localhost:3000/`<file_name>`.

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.use(express.static(`<name_of_folder>`));

app.listen(port, () => console.log(`listening on port ${port}!`));
```

## Fetch Recap

[using fetch MDN](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)

## Pokedex Hackathon
