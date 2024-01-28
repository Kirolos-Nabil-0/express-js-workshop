---
title: Introduction
description: Docs intro
layout: ../../layouts/MainLayout.astro
---

# express js

express js framework is a backend framework built with JavaScript runs on nodeJS env

## Getting started

### create new express app using npm


To get started install node and  [npm](https://nodejs.org/en "nodejs")

open up your terminal and

write:

```js
npm init --y
npm i express
```

### writing your server on express
#### index.js
```js
import express from 'express'
const app = express()
const port = 3000
app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```




### what is an endpoint and  createing first endpoint

#### what is an endpoint?

an endpoint is a url that you can access to get data from the server
to write your first endpoint you need to write this code in your index.js file

```js
app.get('/', (req, res) => {
  res.send('Hello World!')
})

```
congrats you just wrote your first endpoint


