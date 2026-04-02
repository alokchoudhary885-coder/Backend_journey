# 🚀 Node.js — Core Concepts (Day 2)

---

## 🔹 REPL

REPL = Read Eval Print Loop

- Run JavaScript in terminal
- Start: node
- Exit: .exit or Ctrl + C

Example:
> 2 + 3
5

---

## 🔹 File System (fs)

Used to handle files in Node.js

- writeFileSync → create file  
- readFileSync → read file  
- appendFileSync → update file  
- unlinkSync → delete file  

Example:
```js
const fs = require('fs')
fs.writeFileSync("test.txt", "Hello")
🔹 Process

Global object

process.argv → command line input
process.env → environment variables
process.exit() → stop program
🔹 module.exports

Used to export data from one file

Example:

function add(a, b) {
  return a + b;
}

module.exports = add;

Import:

const add = require("./math")
🔹 Export in Directory

Use index.js to combine exports

Example:

const add = require("./add")
const sub = require("./sub")

module.exports = { add, sub }
🔹 NPM

Node Package Manager

npm init → create project
npm install → install packages
🔹 Installing Package
npm install express
npm install -g nodemon
🔹 package.json

Stores project information

name
version
scripts
dependencies
🔹 Local vs Global
Local → project specific
Global → system wide
🔹 Import Module
require("./file")   // local
require("express")  // package
🔹 Important Notes
Node.js uses module system
NPM manages dependencies
Backend development ka base hai