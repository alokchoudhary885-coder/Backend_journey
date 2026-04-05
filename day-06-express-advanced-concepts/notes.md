# 🚀 Express.js — Advanced Concepts (Day 6)

---

## 🔹 Installing Nodemon

### 📌 What is Nodemon?

Nodemon is a development tool that automatically restarts the Node.js server whenever you make changes in your code.

---

### 📌 Why use Nodemon?

- No need to manually restart the server  
- Saves development time  
- Improves productivity  
- Useful during API and backend development  

---

### 📌 Installation

#### Local Installation (Recommended)

```bash
npm install nodemon --save-dev
Global Installation
npm install -g nodemon
📌 Running Server with Nodemon
npx nodemon app.js

👉 If installed globally:

nodemon app.js
📌 Example
const express = require("express");
const app = express();

app.get("/", (req, res) => {
  res.send("Hello Nodemon");
});

app.listen(3000, () => {
  console.log("Server running on port 3000");
});
📌 Output

Terminal:

[nodemon] starting node app.js

Browser:

http://localhost:3000 → Hello Nodemon

👉 When you change code → server restarts automatically

📌 package.json Script (Best Practice)
"scripts": {
  "dev": "nodemon app.js"
}

Run using:

npm run dev
🧠 One Line

Nodemon automatically restarts the server when code changes.

🔹 Path Parameters
📌 What are Path Parameters?

Path parameters are dynamic values present in the URL, used to send data from the client to the server.

📌 Syntax
/user/:id

👉 :id is a dynamic parameter

📌 Example
const express = require("express");
const app = express();

app.get("/user/:id", (req, res) => {
  res.send(req.params.id);
});

app.listen(3000);
📌 Output
http://localhost:3000/user/101 → 101
📌 How it works
:id captures value from URL
Value is stored in req.params
Access using req.params.id
📌 Multiple Parameters
app.get("/user/:id/:name", (req, res) => {
  res.send(req.params);
});
📌 Output
http://localhost:3000/user/101/alok  
→ { id: "101", name: "alok" }
📌 Use Cases
Fetch user by ID
Product details page
Dynamic routes in APIs
📌 Important Points
Defined using : (colon)
Access using req.params
Used in REST APIs
Always string type
🧠 One Line

Path parameters allow passing dynamic values in the URL and accessing them using req.params.

🎯 Summary
Nodemon → Auto-restarts server during development
Path Parameters → Used to send dynamic data through URL