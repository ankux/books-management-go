# Books Management API in Go

This is a simple RESTful API personal project built using Go (Golang) for managing books. It supports CRUD operations and is designed with clean architecture principles.

## Features

- Add new books
- Get all books or a specific book by ID
- Update book details
- Delete a book

## Project Structure

```
.
books-management-go/
├── cmd/
│   └── main/
│       ├── main.go
├── pkg/
│   ├── config/
│   │   └── app.go
│   ├── controllers/
│   │   └── book-controller.go
│   ├── models/
│   │   └── book.go
│   ├── routes/
│   │   └── bookstore-routes.go
│   └── utils/
│       └── utils.go
├── go.mod
└── go.sum
```

## Installation

Make sure you have Go installed. You can download it from [https://golang.org/dl/](https://golang.org/dl/).

Clone the repository and navigate into it:

```bash
git clone https://github.com/yourusername/book-management-api.git
cd book-management-api
```

Install dependencies:

```bash
go mod tidy
```

## Running the Project

Make sure to create a database named `books` in your local MySQL database.

To build the project:

```bash
go build
```

To run the API server:

```bash
go run main.go
```

The server will start on `http://localhost:8080`.

## API Endpoints

| Method | Endpoint          | Description          |
|--------|-------------------|----------------------|
| GET    | `/books`          | Get all books        |
| GET    | `/books/{id}`     | Get book by ID       |
| POST   | `/books`          | Add a new book       |
| PUT    | `/books/{id}`     | Update book details  |
| DELETE | `/books/{id}`     | Delete a book        |

## Example Book JSON

```json
{
  "title": "Go Programming",
  "author": "Robert Griesemer, Rob Pike, and Ken Thompson",
  "publication": "Google"
}
```