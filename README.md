# Go Simple Post API

This is a basic RESTful API written in Go that allows you to create, retrieve, and delete posts. It demonstrates basic CRUD operations using in-memory storage.

## Features

- **GET** all posts
- **POST** a new post
- **GET** a specific post by ID
- **DELETE** a post by ID

## Requirements

- Go 1.23 or higher

## Installation

1. Clone the repository:

```bash
  git clone https://github.com/your-username/go-simple-post-api.git
```

2. Navigate into the project directory:

```bash
  cd go-server
```

3. Build the application:

```bash
  go build
```

## Running the Server

```bash
  go run main.go
```
The server will start at http://localhost:8080.

## API Endpoints

### Get All Posts

* **URL:** `/posts`
* **Method:** `GET`
* **Description:** Retrieves all posts.

```bash
  curl -X GET http://localhost:8080/posts
```

### Create a New Post

* **URL:** `/posts`
* **Method:** `POST`
* **Description:** Creates a new post with a JSON body.
* **Request Body:**

```json
{
  "body": "Your post content"
}
```

```bash
  curl -X POST http://localhost:8080/posts \
  -H "Content-Type: application/json" \
  -d '{"body": "My first post"}'
```

### Get a Post by ID

* **URL:** `/posts/{id}`
* **Method:** `GET`
* **Description:** Retrieves a specific post by its ID.

```bash
  curl -X GET http://localhost:8080/post/1
```

### Delete a Post by ID

* **URL:** `/posts/{id}`
* **Method:** `DELETE`
* **Description:** Deletes a post by its ID.

```bash
  curl -X DELETE http://localhost:8080/post/1
```
