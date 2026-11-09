# 📘 Assignment: Building REST APIs with FastAPI

## 🎯 Objective

Build a small REST API with FastAPI and practice designing endpoints, handling CRUD operations, validating request data, and returning appropriate HTTP status codes.

## 📝 Tasks

### 🛠️ Create a FastAPI Service

#### Description
Create a FastAPI application that can be started locally and responds to a health-check request.

#### Requirements
Completed program should:

- Create a `main.py` file with a FastAPI application instance
- Provide a `GET /health` endpoint that returns `{"status": "ok"}`
- Run locally with `uvicorn main:app --reload`
- Open the interactive API documentation at `/docs`


### 🛠️ Build Book CRUD Endpoints

#### Description
Add endpoints to create, read, update, and delete books. Store books in memory; each book should have an ID, a title, and an author.

#### Requirements
Completed program should:

- Provide `GET /books` to return all books and `POST /books` to create a book
- Provide `GET /books/{book_id}`, `PUT /books/{book_id}`, and `DELETE /books/{book_id}` for an individual book
- Generate a unique ID for each new book
- Return `201 Created` when a book is created and `404 Not Found` when a requested book does not exist


### 🛠️ Validate Requests and Check Responses

#### Description
Use FastAPI request models to validate book data, then test each endpoint using the interactive documentation or an HTTP client.

#### Requirements
Completed program should:

- Define a request model requiring non-empty `title` and `author` values
- Return a validation error for requests with missing or invalid fields
- Return `204 No Content` after successfully deleting a book
- Demonstrate successful create, list, retrieve, update, and delete requests, plus a `404` response for an unknown book ID
