# 📘 Assignment: Testing FastAPI with pytest

## 🎯 Objective

Write automated tests for the book API from the FastAPI assignment. Use pytest and FastAPI's TestClient to verify successful requests, validation errors, and not-found responses.

## 📝 Tasks

### 🛠️ Set Up an API Test

#### Description
Install the test tools and write a first test for the existing health-check endpoint.

#### Requirements
Completed program should:

- Install pytest and httpx with `python -m pip install pytest httpx`
- Create a `test_main.py` file that imports the FastAPI app and `TestClient`
- Use `TestClient` to send `GET /health` and assert a `200` response with `{"status": "ok"}`
- Run the test with `python -m pytest`


### 🛠️ Test a Book's CRUD Lifecycle

#### Description
Write a test that creates a book through the API, uses the returned ID to retrieve and update it, and then deletes it.

#### Requirements
Completed program should:

- Assert that creating a book returns `201 Created` and the expected title and author
- Assert that the created book appears in `GET /books` and can be retrieved with `GET /books/{book_id}`
- Assert that updating the book changes its data and returns the expected success status
- Assert that deleting the book returns `204 No Content`
- Avoid assuming the book list is empty; create the records needed by the test through API requests


### 🛠️ Test Invalid and Missing Books

#### Description
Add tests for invalid book data and requests that use a book ID that does not exist.

#### Requirements
Completed program should:

- Assert that a request with a missing or empty required field returns `422 Unprocessable Entity`
- Assert that requesting a book with a valid but unused ID returns `404 Not Found`
- Cover at least one missing-book case for each of `GET`, `PUT`, and `DELETE`
- Pass repeatedly without depending on test execution order or previously stored books
