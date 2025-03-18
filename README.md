# Spring Boot CRUD Application

## Overview

This is a simple Spring Boot application that demonstrates CRUD (Create, Read, Update, Delete) operations using Spring Data JPA and PostgreSQL database. The application also includes unit tests using JUnit and Mockito.

### Technologies Used

Spring Boot - Framework for building Java applications.

Spring Data JPA - Simplifies database interactions.

PostgreSQL - Relational database for development and production.

Spring Boot Test, JUnit, Mockito - Testing frameworks.

Maven - Dependency management.

### Prerequisites

Before running the application, ensure you have:

Java 22 installed.

Maven installed.

PostgreSQL installed and running.

An IDE like IntelliJ IDEA or Eclipse (optional but recommended).

## How to Run the Project

Clone the Repository:

git clone <repository-url>
cd spring-boot-crud

Configure PostgreSQL Database:
Update the application.properties file with your PostgreSQL credentials:

spring.datasource.url=jdbc:postgresql://localhost:5432/your_database <br/>
spring.datasource.username=your_username <br/>
spring.datasource.password=your_password <br/>
spring.datasource.driverClassName=org.postgresql.Driver <br/>
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect <br/>
spring.jpa.hibernate.ddl-auto=update

- Build the Project: mvn clean install

- Run the Application: mvn spring-boot:run

The application will start at http://localhost:8080.

### API Endpoints

## Employee CRUD Operations 

<ins>Create a new Employee</ins>

URL: /employees

Method: POST

Request Body:

{
  "name": "John Doe",
  "email": "johndoe@example.com",
  "position": "Software Engineer"
}

Response:

{
  "id": 1,
  "name": "John Doe",
  "email": "johndoe@example.com",
  "position": "Software Engineer"
}

<ins>Get an Employee by ID</ins>

URL: /employees/{id}

Method: GET

Response:

{
  "id": 1,
  "name": "John Doe",
  "email": "johndoe@example.com",
  "position": "Software Engineer"
}

<ins>Update an Employee </ins>

URL: /employees/{id}

Method: PUT

Request Body:

{
  "name": "John Doe Updated",
  "email": "john.updated@example.com",
  "position": "Senior Software Engineer"
}

Response:

{
  "id": 1,
  "name": "John Doe Updated",
  "email": "john.updated@example.com",
  "position": "Senior Software Engineer"
}

<ins>Delete an Employee </ins>

URL: /employees/{id}

Method: DELETE

Response: 204 No Content

### Running Tests
To execute the unit tests, run: mvn test
