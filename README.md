# Library Management System

## Overview
The **Library Management System** is a RESTful API built using **Spring Boot**, **Spring Data JPA (Hibernate)**, and **MySQL**. This system allows users to manage library operations such as adding books, managing users, borrowing and returning books.

## Features
- Create a new user
- Fetch all users
- Add a new book
- Fetch all books
- Fetch a specific book
- Delete a book
- Borrow a book
- Return a book

## Technologies Used
- **Spring Boot** - Backend framework
- **Spring Data JPA (Hibernate)** - ORM for database interactions
- **MySQL** - Relational database
- **Spring Boot Starter Web** - For building REST APIs
- **Lombok** - To reduce boilerplate code
- **Swagger** - API Documentation

## Prerequisites
Make sure you have the following installed:
- **Java 17 or later**
- **Maven**
- **MySQL Server**
- **Postman** (optional for testing API endpoints)

## Getting Started

### 1. Clone the Repository
```sh
git clone https://github.com/your-username/library-management-system.git
cd library-management-system
```

### 2. Configure Database
- Update **application.properties** file with your MySQL credentials:
  ```properties
  spring.datasource.url=jdbc:mysql://localhost:3306/library_db
  spring.datasource.username=root
  spring.datasource.password=yourpassword
  spring.jpa.hibernate.ddl-auto=update
  ```

### 3. Build and Run the Application
```sh
mvn spring-boot:run
```

### 4. Access the API
Once the application is running, you can access the endpoints:
- API Base URL: `http://localhost:8080/api`
- Swagger Documentation: `http://localhost:8080/swagger-ui.html`

## API Endpoints
| Method | Endpoint               | Description          |
|--------|------------------------|----------------------|
| POST   | `/users`               | Create a new user   |
| GET    | `/users`               | Fetch all users     |
| POST   | `/books`               | Add a new book      |
| GET    | `/books`               | Fetch all books     |
| GET    | `/books/{id}`          | Fetch a specific book |
| DELETE | `/books/{id}`          | Delete a book       |
| POST   | `/books/{id}/borrow`   | Borrow a book       |
| POST   | `/books/{id}/return`   | Return a book       |

## Testing the API
Use **Postman** or **Swagger UI** to test the API endpoints.

## Future Enhancements
- Implement authentication and authorization (Spring Security, JWT)
- Add fine calculation for overdue books
- Implement email notifications for due dates

## Import postman 
- import the json file in postman to run API's
