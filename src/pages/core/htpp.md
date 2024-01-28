---
layout: ../../layouts/MainLayout.astro

---

<h1>htpp methods </h1>

## what is an http method?

http methods are the methods that you can use to operate on  data on the server

## what are the http methods?

### GET
We use the GET method to get data from the server

### POST
We use the POST method to send data to the server

### PUT
We use the PUT method to update data on the server

### DELETE

We use the DELETE method to delete data from the server

### PATCH

We use the PATCH method to update data on the server

### OPTIONS

We use the OPTIONS method to get the options of a request

## how to use http methods in express

### GET

```js
app.get('/', (req, res) => {
  res.send('Hello World!')
})
```

### POST

```js
app.post('/', (req, res) => {
  res.send('Hello World!')
})
```

### PUT

```js
app.put('/', (req, res) => {
  res.send('Hello World!')
})
```

### DELETE

```js
app.delete('/', (req, res) => {
  res.send('Hello World!')
})
```

### PATCH

```js
app.patch('/', (req, res) => {
  res.send('Hello World!')
})
```

### OPTIONS

```js
app.options('/', (req, res) => {
  res.send('Hello World!')
})
```

## what is a route?

a route is a path that you can access to get data from the server

## how to write a route in express

```js
app.get('/', (req, res) => {
  res.send('Hello World!')
})
```
