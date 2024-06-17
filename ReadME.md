# HTTP-SERVER 

This repository contains a simple HTTP server written in Go (`go-server`) that manages posts using JSON for data exchange.

## Module: `go-server`

- **Go Version:** 1.22.0
- **Package:** `main`

## Description

The server manages posts through HTTP endpoints (`/posts` and `/posts/{id}`) allowing basic CRUD operations (Create, Read, Update, Delete). Posts are stored in memory and accessed concurrently using mutex locks.

## Endpoints

- **GET /posts:** Retrieve all posts.
- **POST /posts:** Create a new post.
- **GET /posts/{id}:** Retrieve a specific post by ID.
- **DELETE /posts/{id}:** Delete a post by ID.

## Usage

1. **Running the Server:**
   ```
   go run .
   ```
   The server will start at `http://localhost:8080`.

2. **Endpoints:**
   - **GET http://localhost:8080/posts:** Retrieves all posts.
   - **POST http://localhost:8080/posts:** Creates a new post.
     - Example POST body: `{"body": "Example post body"}`
   - **GET http://localhost:8080/posts/{id}:** Retrieves a specific post by ID.
   - **DELETE http://localhost:8080/posts/{id}:** Deletes a post by ID.

## Testing

The repository includes unit tests using Go's testing framework (`testing`). Tests validate the functionality of handling GET and POST requests to `/posts`, as well as handling DELETE requests to `/posts/{id}`.

To run the tests:
```
go test -v
```

### Packages Used

- `encoding/json`: For JSON encoding and decoding.
- `fmt`: For formatted printing.
- `io`: For basic input/output operations.
- `log`: For logging errors.
- `net/http`: For HTTP server and client implementations.
- `strconv`: For string conversions.
- `sync`: For providing basic synchronization primitives.
