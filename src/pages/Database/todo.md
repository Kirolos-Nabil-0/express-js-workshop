---
title: "Todo app"
layout: "../../layouts/MainLayout.astro"
---

# Todo app

## setup express


### create index.js

```js

import express from 'express'
const app = express()
const port = 3000


app.use(express.json())
// express.json() is a middleware that parses the body of the request and converts it to json
app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})
```



## setup routes 


### create todo

```js
app.post('/todo', (req, res) => {
  const todo = new Todo({
    title: req.body.title,
    description: req.body.description,
    completed: req.body.completed
  })
  todo.save()
  res.send(todo)
})
```

### get all todos

```js

app.get('/todo', async (req, res) => {
  const todos = await Todo.find()
  res.send(todos)
})
```

### get todo by id

```js
app.get('/todo/:id', async (req, res) => {
  const todo = await Todo.findById(req.params.id)
  res.send(todo)
})
```

### update todo by id

```js
app.put('/todo/:id', async (req, res) => {
  const todo = await Todo.findById(req.params.id)
  todo.title = req.body.title
  todo.description = req.body.description
  todo.completed = req.body.completed
  todo.save()
  res.send(todo)
})
```

### delete todo by id

```js
app.delete('/todo/:id', async (req, res) => {
  const todo = await Todo.findById(req.params.id)
  todo.delete()
  res.send(todo)
})
```

## final index.js

```js
import express from 'express'
import mongoose from 'mongoose'
import Todo from './models/todo.js'
const app = express()
const port = 3000

mongoose.connect('mongodb://localhost:27017/todo', {useNewUrlParser: true, useUnifiedTopology: true})

app.use(express.json())
// express.json() is a middleware that parses the body of the request and converts it to json

app.post('/todo', (req, res) => {
  const todo = new Todo({
    title: req.body.title,
    description: req.body.description,
    completed: req.body.completed
  })
  todo.save()
  res.send(todo)
})

app.get('/todo', async (req, res) => {
  const todos = await Todo.find()
  res.send(todos)
})

app.get('/todo/:id', async (req, res) => {
  const todo = await Todo.findById(req.params.id)
  res.send(todo)
})


app.put('/todo/:id', async (req, res) => {
  const todo = await Todo.findById(req.params.id)
  todo.title = req.body.title
  todo.description = req.body.description
  todo.completed = req.body.completed
  todo.save()
  res.send(todo)
})

app.delete('/todo/:id', async (req, res) => {
  const todo = await Todo.findById(req.params.id)
  todo.delete()
  res.send(todo)
})


app.listen(port, () => {
  console.log(`Example app listening at http://localhost:${port}`)
})

```














