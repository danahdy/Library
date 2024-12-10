# Library API

This is a Library API built using PHP, Slim framework, Firebase JWT for authentication, and MySQL for database management.

## Prerequisites

- PHP 7.4 or higher
- Composer
- MySQL
- Slim Framework
- Firebase JWT

## Endpoints

### User Registration

- **URL:** `/user/register`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "username": "string",
        "password": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": null
    }
    ```

### User Login

- **URL:** `/user/login`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "username": "string",
        "password": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": {
            "token": "string"
        }
    }
    ```

### User Authentication

- **URL:** `/user/auth`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "token": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": {
            "username": "string",
            "password": "string"
        }
    }
    ```

### View Employee

- **URL:** `/user/viewEmployee`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "token": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": {
            "username": "string",
            "password": "string"
        }
    }
    ```

### Author Registration

- **URL:** `/author/register`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "username": "string",
        "password": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "Author Registered Successfully",
        "data": null
    }
    ```

### Author Login

- **URL:** `/author/login`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "username": "string",
        "password": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "Author Log In Successfully",
        "data": {
            "token": "string"
        }
    }
    ```

### Author Authentication

- **URL:** `/author/auth`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "username": "string",
        "password": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "Author Authenticated",
        "data": {
            "token": "string"
        }
    }
    ```

### Post Book

- **URL:** `/author/postBook`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "token": "string",
        "title": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": {
            "message": "Book posted successfully"
        }
    }
    ```

### View All Books

- **URL:** `/books/viewallbooks`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "token": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": [
            {
                "bookid": "integer",
                "title": "string"
            }
        ]
    }
    ```

### View All Authors

- **URL:** `/author/viewallauthor`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "token": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": [
            {
                "authorid": "integer",
                "username": "string"
            }
        ]
    }
    ```

### Delete Book

- **URL:** `/books/delete`
- **Method:** `DELETE`
- **Payload:**
    ```json
    {
        "bookid": "integer",
        "token": "string"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": {
            "title": "Book deleted successfully"
        }
    }
    ```

### View Book by Author

- **URL:** `/books/author/view`
- **Method:** `POST`
- **Payload:**
    ```json
    {
        "token": "string",
        "authorid": "integer",
        "bookid": "integer"
    }
    ```
- **Response:**
    ```json
    {
        "status": "success",
        "data": {
            "book": {
                "id": "integer",
                "title": "string"
            }
        }
    }
    ```

## License

This project is licensed under the MIT License.
