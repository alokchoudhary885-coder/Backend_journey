# 🚀 Express.js — Introduction

## 🔹 What is Express.js?
Express.js is a framework for Node.js used to build servers and APIs easily.

---

## 🔹 Basic Server

```js
const express = require("express");
const app = express();

app.listen(3000, () => {
  console.log("Server started");
});
Output

Server started