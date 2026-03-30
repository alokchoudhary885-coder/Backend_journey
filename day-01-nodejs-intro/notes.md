# 🚀 Node.js — Basics & Introduction

## 🔹 What is Node.js?
Node.js is a **JavaScript runtime environment** built on Chrome’s V8 engine that allows running JavaScript on the server side.

---

## 🔹 Key Features
- Single-threaded  
- Non-blocking (Asynchronous)  
- Event-driven architecture  
- Fast execution (V8 engine)  

---

## 🔹 Why Use Node.js?
- High performance  
- Scalable applications  
- Same language (JavaScript) for frontend & backend  

---

## 🔹 Use Cases
- REST APIs  
- Real-time apps (chat, live updates)  
- Streaming applications  

---

## 🔹 Core Concepts
- Event Loop  
- Callback, Promises, Async/Await  
- Non-blocking I/O  

---

## 🔹 Modules
- Built-in modules: `http`, `fs`  
- Import example:
```js
const fs = require('fs')


🔹 npm (Node Package Manager)
npm init -y
npm install express
🔹 Basic Server Example
const http = require('http')

http.createServer((req, res) => {
  res.end("Hello World")
}).listen(3000)
🔹 Important Note ⚠️

Node.js is best for I/O-heavy tasks (APIs, real-time apps)
❌ Not suitable for CPU-intensive tasks (heavy calculations, video processing)
