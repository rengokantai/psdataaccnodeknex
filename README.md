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
### Tips for Development
```
module.exports = 
{
 pg:{
  client:"pg",
  connection:{
    host:'localhost',
    user: 'postgres',
    database:'book',
    password:''
    },
    sqlite:{
     client: "sqlite3",
  connection:{
    filename: "./book.sqlite"
  }
    }
    
}
```
screen.js
```
var screen = {
 clear:function(){
  process.stdout.write("\033c");
 }
}
```
####07:45
```
npm install prettyjson --save
```
in screen.js
```
var prettyjson = requrie("prettyjson");
ops ={
 keysColor:"",
 dashColor:"",
 stringColor:"",
 numberColor:""
};
output=prettyjson.render(data);
```

####10:45
```
var query = knex.select("title","rating").from("book");
var sql = query.toString();
console.log(sql);
```



##2. Building Queries 
###1 Querying with Promises
```
knex.select/column("title","rating").from/table("book").then(function(rows){},function(){
});
```






