---
title: "Database introduction"
layout: "../../layouts/MainLayout.astro"

---
# Database introduction
## What is a database?
A database is an organized collection of data, generally stored and accessed electronically from a computer system. Where databases are more complex they are often developed using formal design and modeling techniques.

## why to not use files instead of databases?
### why to use databases?
- databases are faster than files
- databases are more secure than files
- databases are more organized than files
- databases are more scalable than files
- databases are more reliable than files
- databases are more efficient than files
- databases are more flexible than files
- databases are more portable than files
- databases are more manageable than files

## Types of databases
### Relational databases
A relational database is a type of database that stores and provides access to data points that are related to one another. Relational databases are based on the relational model, an intuitive, straightforward way of representing data in tables. In a relational database, each row in the table is a record with a unique ID called the key. The columns of the table hold attributes of the data, and each record usually has a value for each attribute, making it easy to establish the relationships among data points.

### Non-relational databases
A non-relational database is a database that does not incorporate the table/key model that relational database management systems (RDBMS) promote. Instead, non-relational databases use a storage model that is optimized for the specific requirements of the type of data being stored. Non-relational databases are also referred to as NoSQL databases — with the SQL referring to structured query language that is used to communicate with relational databases.


## what we will use in this course?
we will use mongodb as our database

## what is mongodb?
MongoDB is a general purpose, document-based, distributed database built for modern application developers and for the cloud era. No database makes you more productive.

## how to use mongodb?
### install mongodb
to install mongodb go to [mongodb.com](https://www.mongodb.com/try/download/community "mongodb.com") and download the version that fits your os

### mongoose in express

#### install mongoose
to install mongoose write this command in your terminal
```js
$ npm i mongoose
```

#### connect to mongodb
to connect to mongodb write this code in your index.js file
```js
import mongoose from 'mongoose'
mongoose.connect('mongodb://localhost:27017/todo', {useNewUrlParser: true, useUnifiedTopology: true})
```

