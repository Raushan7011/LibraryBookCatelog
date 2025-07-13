Library Book Catalog – Spring Boot REST API
This is a simple Spring Boot RESTful application that allows users to manage a library’s book catalog. It uses in-memory List storage, so no database is required.

GitHub Repo: LibraryBookCatelog

Features
Add a new book
Get all books
Get a book by ID
Delete a book
Update book availability
Technologies Used
Java 17
Spring Boot 3.3.x
Jakarta Bean Validation
Maven
Git + GitHub
How to Run the Project
1. Clone the Repository
git clone https://github.com/Yashvant1221/LibraryBookCatelog.git
cd LibraryBookCatelog


1. Add a Book
Endpoint: POST /addBook

Request:

{
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "isbn": "9780132350884",
  "available": true
}
Response :

{
  "id": 1,
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "isbn": "9780132350884",
  "available": true
}

2. Get All Books
Endpoint: GET /getAllBooks

Response (200 OK):

[
  {
    "id": 1,
    "title": "Clean Code",
    "author": "Robert C. Martin",
    "isbn": "9780132350884",
    "available": true
  },
  {
    "id": 2,
    "title": "Effective Java",
    "author": "Joshua Bloch",
    "isbn": "9780134685991",
    "available": false
  }
]

3. Get Book by ID
Endpoint: GET /getBookById/{id}
Example: /getBookById/1

Response (200 OK):

{
  "id": 1,
  "title": "Clean Code",
  "author": "Robert C. Martin",
  "isbn": "9780132350884",
  "available": true
}

4. Delete Book by ID
Endpoint: DELETE /deleteBook/{id}
Example: /deleteBook/1

Response :
Book is deleted by Id : bookId

5. Update Availability
Endpoint: PATCH /{id}/availability?available={true|false}
Example: /2/availability?available=false

Response :

{
  "id": 2,
  "title": "Effective Java",
  "author": "Joshua Bloch",
  "isbn": "9780134685991",
  "available": false
}
