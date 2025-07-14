# TaskMaster API

![Java](https://img.shields.io/badge/Java-17-blue.svg)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3.1-green.svg)
![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

> A simple and efficient REST API for task management, built with the Spring Boot framework. This project provides a complete backend solution for a to-do list application, including user authentication and full CRUD functionality for tasks.

## 📜 Overview

TaskMaster API is a backend service designed to handle all the logic for a modern task management application. It's built following REST principles and is secured using Spring Security with JWT (JSON Web Tokens) for authentication. It's designed to be stateless, scalable, and easy to connect with any frontend application (like React, Angular, or Vue.js).

## ✨ Features

* **User Authentication**: Secure user registration and login endpoints using JWT.
* **CRUD Operations for Tasks**: Full support for Creating, Reading, Updating, and Deleting tasks.
* **Task Management**: Assign tasks to users, set due dates, and update task statuses (e.g., 'pending', 'completed').
* **User-Specific Data**: Users can only view and manage their own tasks.
* **Database Profiles**: Uses an in-memory H2 database for easy local development and a PostgreSQL profile for production.
* **Validation**: Input validation for user registration and task creation to ensure data integrity.

## 🛠️ Tech Stack

* **Framework**: Spring Boot 3.3.1
* **Language**: Java 17
* **Security**: Spring Security 6, JSON Web Tokens (JWT)
* **Data Persistence**: Spring Data JPA (Hibernate)
* **Database**: H2 (for development), PostgreSQL (for production)
* **Build Tool**: Apache Maven
* **Testing**: JUnit 5, Mockito

## 🚀 Getting Started

Follow these instructions to get the project up and running on your local machine for development and testing purposes.

### Prerequisites

* JDK (Java Development Kit) 17 or later
* Apache Maven
* An IDE like IntelliJ IDEA or VS Code

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YOUR_USERNAME]/[YOUR_REPOSITORY_NAME].git
    ```

2.  **Navigate to the project directory:**
    ```bash
    cd [YOUR_REPOSITORY_NAME]
    ```

3.  **Build the project and install dependencies:**
    ```bash
    mvn clean install
    ```

4.  **Run the application:**
    ```bash
    mvn spring-boot:run
    ```

The API will start on `http://localhost:8080`. By default, it uses the `dev` profile with the H2 in-memory database.

## 📡 API Endpoints

The base URL for all endpoints is `/api`.

### Authentication

| Method | Endpoint         | Description                   |
|--------|------------------|-------------------------------|
| `POST` | `/auth/register` | Registers a new user.         |
| `POST` | `/auth/login`    | Authenticates a user and returns a JWT. |

### Tasks (Requires Authentication)

All endpoints below require a valid JWT in the `Authorization: Bearer <token>` header.

| Method | Endpoint      | Description                       |
|--------|---------------|-----------------------------------|
| `GET`  | `/tasks`      | Get all tasks for the logged-in user. |
| `GET`  | `/tasks/{id}` | Get a specific task by its ID.      |
| `POST` | `/tasks`      | Create a new task.                |
| `PUT`  | `/tasks/{id}` | Update an existing task.          |
| `DELETE`| `/tasks/{id}`| Delete a task.                    |

---
This project was created for portfolio and learning purposes.
