---
title: handlers
description: handlers in expressjs
layout: ../../layouts/MainLayout.astro
---

# handlers in expressjs
## What is a handler?
A handler is a function that has access to the request object (req), the response object (res), 
and its the end of the request-response cycle. There is no next function in the handler function.

## How does a handler work?

A handler function can perform the following tasks:

Execute any code.
Make changes to the request and the response objects.
End the request-response cycle.
If the current handler function does not end the request-response cycle, it must call res.end() to end the request-response cycle. Otherwise, the request will be left hanging.


## middleware vs handler

middleware is a function that has access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.

A handler is a function that has access to the request object (req), the response object (res), and its the end of the request-response cycle. There is no next function in the handler function.

## example for handler with middleware

```js
import express from 'express'
const app = express()
const port = 3000
app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})


// middleware

function isEven(req, res, next) {
  if (req.params.number % 2 === 0) {
    next()
  } else {
    res.send('not even')
  }
}

// handler

app.get('/:number', isEven, (req, res) => {
  res.send('even')
})

```



