# 🚀 Express.js — Request & Response (Day 5)

---

## 🔹 What is Request & Response?

Client (browser) server ko request bhejta hai  
Server response bhejta hai

---

## 🔹 Handling Request

```js
const express = require("express");
const app = express();

app.get("/", (req, res) => {
  res.send("Hello User");
});

app.listen(3000);
Output

http://localhost:3000
 → Hello User

One Line

Server request receive karta hai aur response deta hai

🔹 Sending Response (Text)
app.get("/data", (req, res) => {
  res.send("Data sent");
});
Output

/data → Data sent

One Line

Server client ko text response bhejta hai

🔹 JSON Response
app.get("/api", (req, res) => {
  res.json({ name: "Alok", age: 21 });
});
Output

{"name":"Alok","age":21}

One Line

Server JSON data send karta hai (API)

🔹 Status Code
app.get("/error", (req, res) => {
  res.status(404).send("Page Not Found");
});
Output

Page Not Found

One Line

Server status code ke sath response bhejta hai

🔹 Query Params
app.get("/search", (req, res) => {
  res.send(req.query.name);
});
Output

/search?name=alok → alok

One Line

URL se query data access kar sakte hain

🔹 Important Points
req → request data
res → response bhejne ke liye
res.send() → text
res.json() → JSON
res.status() → status code
🎯 Summary

Request → Server → Response