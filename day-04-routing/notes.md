# 🚀 Express.js — Routing (Day 4)

---

## 🔹 What is Routing?

Routing means handling different URLs with different responses.

---

## 🔹 Basic Route

```js
const express = require("express");
const app = express();

app.get("/", (req, res) => {
  res.send("Home Page");
});

app.listen(3000);
Output

http://localhost:3000
 → Home Page

One Line

"/" route pe request aane par Home Page show hota hai

🔹 Multiple Routes
app.get("/about", (req, res) => {
  res.send("About Page");
});
Output

http://localhost:3000/about
 → About Page

One Line

Different URLs ke liye different response milta hai

🔹 Route with Params (Dynamic Route)
app.get("/user/:id", (req, res) => {
  res.send(req.params.id);
});
Output

http://localhost:3000/user/101
 → 101

One Line

URL se dynamic value (id) access kar sakte hain

🔹 HTTP Methods
app.post("/data", (req, res) => {
  res.send("Data Received");
});
Output

POST request → Data Received

One Line

Different HTTP methods (GET, POST) ke liye alag routes hote hain

🔹 Important Points
app.get() → GET request
app.post() → POST request
req.params → dynamic route data
Har route ka apna response hota hai