# psdataaccnodeknex
##1. Introduction
###2 What is Knex?
Postgres
```
CREATE TABLE item(id SERIAL);
```
MySQL
```
CREATE TABLE item(id INT NOT NULL AUTO_INCREMENT);
```

###3 Starting a Knex Project
```
npm install pg sqlite3 mysql mariasql strong-oracle --save
```
touch app.js
```
var cfg = {
  client: "sqlite3",
  connection:{
    filename: "./book.sqlite"
  }
}
var knex = require("knex")(cfg);
knex.destroy();
```

###4. Your First Query
```
knex.select("title","rating").from("book").asCallback(function(err,rows){
})
```

pg connection
```
{
  client:"pg",
  connection:{
    host:'localhost',
    user: 'postgres',
    database:'book',
    password:''
    }
}
```
