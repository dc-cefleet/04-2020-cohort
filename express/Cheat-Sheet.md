# Cheat Sheet

## Terms 
* *Port* - is a communication endpoint. For http is an iteger that is between 1 & 65535 that and is always associated with a http address. Default http port is 80 and default https is 443.

* *Route* - A section of Express code that associates an HTTP verb ( GET , POST , PUT , DELETE , etc.), a URL path/pattern, and a function that is called to handle that pattern.

## Code Examples

### Simple (useless) express app.
``` 
const express = require('express');
const app = express();
const port = 8000;

app.listen(port, ()=>console.log(`Listening on port http://localhost:${port}`));
```

### App with Get at root and simple query
```
const express = require('express');
const app = express();
const port = 8000;

app.get("/", (req, res) => {
    res.send(`
<!DOCTYPE HTML>
<html>
    <head>
        <title>Hello World</title>
    </head>
    <body>
        <h1>Hello World!</h1>
        <div>You Requested page : ${req.query.page ? req.query.page : "unknown"}</div>
    </body>
</html>
`)
});
app.listen(8000, () => console.log(`Listening on port http://localhost:${port}`));
```

### Parameters Matching

const express = require('express');
const app = express();
const port = 8000;

app.get("/", (req, res) => res.send("You are at the Home page!"));

app.get("/jedi/:name", (req,res)=>res.send(`Your Jedi Name is ${req.params.name}`))

app.get("/jedi/:name/:age", (req, res=>res.send(`You are a jedi named ${req.params.name} and you are ${req.params.age} years old.`)))
app.listen(8000, () => console.log(`Listening on port http://localhost:${port}`));