# -
Skip to content Learn Git and GitHub without any code! Using the Hello World guide, you’ll start a branch, write comments, and open a pull request.   fadhilsaheer / mongoi Code Issues Pull requests Actions Projects Wiki Security Insights mongoi/readme.md @fadhilsaheer fadhilsaheer added redame  1 contributor 226 lines (143 sloc)  3.64 KB   MONGOI😇 MONGOI is a npm package made by Fadhil  easy tool to manage and do CRUD operation with mongo database  Setup Requirements  Node Js Npm Mongo Db Internet [to download] 😅 npm i mongoi This will install mongoi for you 😎  How To Use Mongoi will help you to do crud operation 😱  to have more features don't forget to contribute 😁  After installing require it  const mongoi = require('mongoi') you have initialize it first  let yourDatabaseConnectionUrl = "mongdb:localhost:27017"  // create database schema as you do for mongoose let databaseSchema = {     name: String, }  let collectionName = "your-collection-name"  mongoi.init(yourDatabaseConnectionUrl, databaseSchema, collectionName).then(()=>{     // you can write anything here except bug 😊 }) now you initialized mongoi successfully 😎  so lets start doing crud 😜  CRUD = CREATE - READ - UPDATE - DELETE  // This is the model of crud 😪  mongoi.crud([option], data).then(()=>{     // use it 😋 })  // options // [you have to write it in string eg : "r"] // // s - "save" // r = "read" // ro = "read one" // u = "update many" // uo = "update one" // d = "delete all" // do = "delete one" // dm = "delete many" //  // Enjoy 🤗 // Create lets create 👻  // create this according to you schema const data_to_save = {     name: "apple",     color: "red" }  mongoi.crud("s". data_to_save) // you can call .then after this 🥱 Read lets read 😏  // read all  mongoi.crud("r").then((data_you_get_from_database)=>{     // do with this data 🐼 }) // read one  let condition = {name: "panda"} // this is the condition of what are you looking for  mongoi.crud("ro", condition).then((data_you_get_from_database)=>{     // do with this data 🐧 }) Update let update 🖊  // update many or update all  let condition_and_data = [     {cute_message: "you are ugly 🤮"},//this should be condition     {cute_message: "you are cute 😘"}//thing you wan't to change ]  mongoi.crud("u", condition_and_data)// you can call .then after this 🥱 i don't care 😏   // 😁  /*  let condition_and_data = [     {cute_message: "you are cute 😘"},//you are not cute 😅     {cute_message: "you are ugly 🤮"}//you are ugly 😁 ]  mongoi.crud("u", condition_and_data)// just kidding 😅  */ // update one  let condition_and_data = [     {cute_message: "you are ugly 🤮"},//this should be condition     {cute_message: "you are cute 😘"}//thing you wan't to change ]  mongoi.crud("uo", condition_and_data)// you can call .then after this 🥱 i don't care 😏   // 😁  /*  let condition_and_data = [     {cute_message: "you are cute 😘"},//you are not cute 😅     {cute_message: "you are ugly 🤮"}//you are ugly 😁 ]  mongoi.crud("u", condition_and_data)// just kidding 😅 Delete lets delete this 🧺  // delete all  mongoi.crud("d") // .then is supported 😇 // delete many  let condition = {cute_message: "you are cute"}  mongoi.crud("dm", condition)// use .then if you want // delete one  let condition = {cute_message: "you are cute"}  mongoi.crud("do", condition)// use .then if you want no one cares 😁 Conclusion Hopefully I assume that you love 💗 this  contribute for updating this garbage 😁  Made With 💗 Fadhil  © 2021 GitHub, Inc. Terms Privacy Security Status Help Contact GitHub Pricing API Training Blog About
Skip to content
Learn Git and GitHub without any code!
Using the Hello World guide, you’ll start a branch, write comments, and open a pull request.


fadhilsaheer
/
mongoi
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
mongoi/readme.md
@fadhilsaheer
fadhilsaheer added redame
 1 contributor
226 lines (143 sloc)  3.64 KB
 
MONGOI😇
MONGOI is a npm package made by Fadhil

easy tool to manage and do CRUD operation with mongo database

Setup
Requirements

Node Js
Npm
Mongo Db
Internet [to download] 😅
npm i mongoi
This will install mongoi for you 😎

How To Use
Mongoi will help you to do crud operation 😱

to have more features don't forget to contribute 😁

After installing require it

const mongoi = require('mongoi')
you have initialize it first

let yourDatabaseConnectionUrl = "mongdb:localhost:27017"

// create database schema as you do for mongoose
let databaseSchema = {
    name: String,
}

let collectionName = "your-collection-name"

mongoi.init(yourDatabaseConnectionUrl, databaseSchema, collectionName).then(()=>{
    // you can write anything here except bug 😊
})
now you initialized mongoi successfully 😎

so lets start doing crud 😜

CRUD = CREATE - READ - UPDATE - DELETE

// This is the model of crud 😪

mongoi.crud([option], data).then(()=>{
    // use it 😋
})

// options
// [you have to write it in string eg : "r"]
//
// s - "save"
// r = "read"
// ro = "read one"
// u = "update many"
// uo = "update one"
// d = "delete all"
// do = "delete one"
// dm = "delete many"
// 
// Enjoy 🤗
//
Create
lets create 👻

// create this according to you schema
const data_to_save = {
    name: "apple",
    color: "red"
}

mongoi.crud("s". data_to_save) // you can call .then after this 🥱
Read
lets read 😏

// read all

mongoi.crud("r").then((data_you_get_from_database)=>{
    // do with this data 🐼
})
// read one

let condition = {name: "panda"} // this is the condition of what are you looking for

mongoi.crud("ro", condition).then((data_you_get_from_database)=>{
    // do with this data 🐧
})
Update
let update 🖊

// update many or update all

let condition_and_data = [
    {cute_message: "you are ugly 🤮"},//this should be condition
    {cute_message: "you are cute 😘"}//thing you wan't to change
]

mongoi.crud("u", condition_and_data)// you can call .then after this 🥱 i don't care 😏


// 😁

/*

let condition_and_data = [
    {cute_message: "you are cute 😘"},//you are not cute 😅
    {cute_message: "you are ugly 🤮"}//you are ugly 😁
]

mongoi.crud("u", condition_and_data)// just kidding 😅

*/
// update one

let condition_and_data = [
    {cute_message: "you are ugly 🤮"},//this should be condition
    {cute_message: "you are cute 😘"}//thing you wan't to change
]

mongoi.crud("uo", condition_and_data)// you can call .then after this 🥱 i don't care 😏


// 😁

/*

let condition_and_data = [
    {cute_message: "you are cute 😘"},//you are not cute 😅
    {cute_message: "you are ugly 🤮"}//you are ugly 😁
]

mongoi.crud("u", condition_and_data)// just kidding 😅
Delete
lets delete this 🧺

// delete all

mongoi.crud("d") // .then is supported 😇
// delete many

let condition = {cute_message: "you are cute"}

mongoi.crud("dm", condition)// use .then if you want
// delete one

let condition = {cute_message: "you are cute"}

mongoi.crud("do", condition)// use .then if you want no one cares 😁
Conclusion
Hopefully I assume that you love 💗 this

contribute for updating this garbage 😁

Made With 💗 Fadhil

© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
