Task 3 – Book API Project

# 📘 Task 3 – Book API Project

This project is a simple RESTful API built with **Node.js** and **Express.js** to manage a list of books.  
It supports basic **CRUD operations** like creating, reading, updating, and deleting book records.



## 📌 Features

- ✅ Get all books
- ✅ Add a new book
- ✅ Update a book by ID
- ✅ Delete a book by ID
- ✅ JSON-based request and response handling


## 🔗 Postman Collection

You can test this API using Postman documentation here:  
👉 [Click to open Postman Docs](https://documenter.getpostman.com/view/45437836/2sB2qfAJyS)


## 🔧 How to Run

### 1️⃣ Install Node.js (if not installed):  
[https://nodejs.org/](https://nodejs.org/)

### 2️⃣ Clone the Repository and Install Dependencies

```bash
git clone https://github.com/sravani12-ui/book-api.git
cd book-api
npm install

3️⃣ Start the Server

node index.js

Server will run at:
📍 http://localhost:3000



🧪 API Endpoints

Method	Endpoint	Description

GET	/books	Get all books
POST	/books	Add a new book
PUT	/books/:id	Update a book by ID
DELETE	/books/:id	Delete a book by ID





📁 Project Structure

book-api/
├── index.js
├── package.json
└── README.md




🙋 Author

Sravani UI
📩 Postman Workspace
📂 GitHub: sravani12-ui




📌 Notes

This project uses in-memory storage, so data will reset every time the server restarts.
For persistent storage, MongoDB or another database can be integrated.




