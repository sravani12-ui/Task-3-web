

📄 index.js – Full Working code

const express = require('express');
const app = express();
const PORT = 3000;

app.use(express.json());

// Dummy in-memory data
let books = [
  { id: 1, title: "Book One", author: "Author A" },
  { id: 2, title: "Book Two", author: "Author B" }
];

// GET: All Books
app.get('/books', (req, res) => {
  res.json(books);
});

// POST: Add a New Book
app.post('/books', (req, res) => {
  const { title, author } = req.body;
  const newBook = {
    id: books.length + 1,
    title,
    author
  };
  books.push(newBook);
  res.status(201).json(newBook);
});

// PUT: Update a Book by ID
app.put('/books/:id', (req, res) => {
  const bookId = parseInt(req.params.id);
  const { title, author } = req.body;
  const book = books.find(b => b.id === bookId);

  if (!book) {
    return res.status(404).json({ message: "Book not found" });
  }

  book.title = title || book.title;
  book.author = author || book.author;
  res.json(book);
});

// DELETE: Remove a Book by ID
app.delete('/books/:id', (req, res) => {
  const bookId = parseInt(req.params.id);
  const bookIndex = books.findIndex(b => b.id === bookId);

  if (bookIndex === -1) {
    return res.status(404).json({ message: "Book not found" });
  }

  books.splice(bookIndex, 1);
  res.json({ message: "Book deleted successfully" });
});

// Start Server
app.listen(PORT, () => {
  console.log(`📚 Book API server running at http://localhost:${PORT}`);
});



