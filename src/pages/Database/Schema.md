---
title: mongoose schema
layout: ../../layouts/MainLayout.astro

---

# mongoose schema

## what is a schema?

A schema is a blueprint of how the database is constructed. A schema is used to define the structure of the database tables and to validate data before it is inserted into the database.

## how to create a schema in mongoose?

src/models/todo.js

```js
import mongoose from 'mongoose'
const todoSchema = new mongoose.Schema({
  title: String,
  description: String,
  completed: Boolean
})
const Todo = mongoose.model('Todo', todoSchema)
export default Todo
```

## what is a model?

A model is a class with which we construct documents. In this case, each document will be a todo with properties and behaviors as declared in our schema. Instances of models are called documents. Models are responsible for creating and reading documents from the underlying MongoDB database.


