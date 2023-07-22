# ToDo App

## Frameworks and Language Used

<p align="center">
<a href="Java url">
    <img alt="Java" src="https://img.shields.io/badge/Java->=8-darkblue.svg" />
</a>
  <a href="Spring Boot url" >
    <img alt="Spring Boot" src="https://img.shields.io/badge/Spring Boot-3.0.6-brightgreen.svg" />
</a>
<a href="Maven url" >
    <img alt="Maven" src="https://img.shields.io/badge/maven-3.0.5-brightgreen.svg" />
</a>
The TodoAPP is developed using the Spring Framework, specifically Spring Boot, for building the backend of the application. The primary language used for development is Java.

## Data Flow

### 1. Controller
The `TodoController` class acts as the entry point for handling incoming HTTP requests and directing them to the appropriate service methods. It contains various endpoints that allow interaction with the Todo entities.

- `getAllTodos()`: This endpoint responds to a GET request to "/todos" and returns a list of all Todo objects available in the application.

- `getDoneTodos()`: This endpoint responds to a GET request to "/todo/done" and returns a list of Todo objects that are marked as done.

- `getTodoById()`: This endpoint responds to a GET request to "/todos/{todoId}" and returns a specific Todo object based on the given todoId.

- `getNotDoneTodos()`: This endpoint responds to a GET request to "/todo/undone" and returns a list of Todo objects that are not marked as done.

- `addTodo()`: This endpoint responds to a POST request to "/todo" and adds a new Todo object to the application based on the provided JSON data in the request body.

- `markTodo()`: This endpoint responds to a PUT request to "/todo/{todoId}/{status}" and updates the status of a specific Todo object identified by todoId.

- `removeTodo()`: This endpoint responds to a DELETE request to "/todo" and removes a Todo object based on the provided todoId in the request parameters.

### 2. Services
The `TodoService` class handles the business logic related to Todo entities. It interacts with the repository layer to perform CRUD operations on the Todo objects.

- `getAllTodos()`: Retrieves all Todo objects from the repository and returns them to the controller.

- `getAllDoneTodos()`: Retrieves all Todo objects marked as done from the repository and returns them to the controller.

- `getTodoById(Integer todoId)`: Retrieves a specific Todo object based on the given todoId from the repository and returns it to the controller.

- `getUndoneTodos()`: Retrieves all Todo objects that are not marked as done from the repository and returns them to the controller.

- `addTodo(Todo todo)`: Adds a new Todo object to the repository using the provided Todo entity.

- `updateTodoStatus(Integer todoId, boolean status)`: Updates the status of a specific Todo object identified by todoId with the provided status value.

- `removeTodo(Integer todoId)`: Removes a Todo object from the repository based on the provided todoId.

## Data Structure Used in Your Project

The primary data structure used in the TodoAPP project is the `Todo` class, representing the individual Todo items. It has three fields: `todoId`, `todoName`, and `isTodoDoneStatus`. These Todo objects are managed and manipulated in lists and collections as needed.

## Project Summary

The TodoAPP is a simple backend application built using the Spring Framework, with Java as the primary programming language. It provides various endpoints to interact with Todo items, allowing users to view all todos, get specific todos, mark them as done or undone, add new todos, and remove existing todos. The project follows a structured data flow pattern, with controllers handling incoming requests, services implementing business logic, and a repository for data access to interact with the underlying database.
