# 🚀 Express.js — EJS & Templating (Day 6)

---

## 🔹 What is Templating?

Templating means generating dynamic HTML using data from the backend.

Instead of writing static HTML, we can inject variables and logic into templates.

---

## 🔹 What is EJS?

EJS (Embedded JavaScript) is a templating engine used with Express to create dynamic HTML pages.

It allows us to write JavaScript inside HTML.

---

## 🔹 Installing EJS

```bash
npm install ejs
🔹 Setup in Express
const express = require("express");
const app = express();

app.set("view engine", "ejs");

👉 This tells Express to use EJS as the templating engine

🔹 Views Directory

The views folder is used to store all template files (.ejs)

Folder Structure
project/
 ├── views/
 │    ├── index.ejs
 │    └── about.ejs
 └── app.js

👉 Express automatically looks inside the views folder

🔹 Rendering a Template
app.get("/", (req, res) => {
  res.render("index", { name: "Alok" });
});

👉 index refers to views/index.ejs

🔹 Example Template (index.ejs)
<h1>Hello <%= name %></h1>
What is this?
✅ Output
Hello Alok
🔹 EJS Syntax
1. Output Variable
<%= name %>
What is this?

👉 Displays value in HTML

2. JavaScript Logic
<% if (name) { %>
  <p>User exists</p>
<% } %>
What is this?
3. Loop
<% users.forEach(user => { %>
  <p><%= user %></p>
<% }) %>
What is this?
🔹 Passing Data from Backend
app.get("/users", (req, res) => {
  const users = ["Alok", "Rahul", "Aman"];
  res.render("index", { users });
});
🔹 Output Example
Alok
Rahul
Aman
🔹 Why use EJS?
Dynamic content rendering
Clean code structure
Reusable templates
Better separation of logic and UI
🔹 Important Points
views folder required
Use res.render() instead of res.send()
Data passed as object
.ejs extension required
🎯 Summary

Templating = HTML + Data
EJS = Templating engine for Express
Views = Folder where templates are stored

🧠 One Line

EJS allows us to generate dynamic HTML using JavaScript inside templates.