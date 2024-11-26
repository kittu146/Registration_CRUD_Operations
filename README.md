# Registration_CRUD_Operations
# Registration API with Spring Boot

A RESTful API for managing user registration information using **Spring Boot**, **Spring Data JPA**, and **MySQL**.

---

## Features

- Create, Read, Update, and Delete (CRUD) operations for registrations.
- Input validation (e.g., name, email, date of birth).
- Global error handling for validation and runtime exceptions.

---

## Technologies

- **Java**, **Spring Boot**, **Spring Data JPA**, **MySQL**
- **Hibernate Validator** for input validation

---

## Getting Started

### Prerequisites

- JDK 17 or later
- MySQL installed and running
- Maven for dependency management

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/registration-api.git
   cd registration-api
Create a MySQL database:

CREATE DATABASE Registration1;
Update src/main/resources/application.properties with your database credentials:

spring.datasource.url=jdbc:mysql://localhost:3306/registration_db
spring.datasource.username=your_username
spring.datasource.password=your_password
Run the application:

mvn spring-boot:run
API Endpoints
Method	Endpoint	Description
POST	/api/registrations	Create a new registration
GET	/api/registrations	Retrieve all registrations
GET	/api/registrations/{id}	Retrieve a registration by ID
PUT	/api/registrations/{id}	Update a registration by ID
DELETE	/api/registrations/{id}	Delete a registration by ID
Example Request: Create Registration
POST /api/registrations
Request Body:

{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "dateOfBirth": "1990-01-01",
  "phoneNumber": "1234567890"
}
Validation Rules
Name: Cannot be blank, max 100 characters.
Email: Must be valid and unique.
Date of Birth: Must be in the past.
Phone Number: Exactly 10 digits and unique.
Testing
Use Postman or cURL for testing. Example:

curl -X POST http://localhost:8080/api/registrations \
-H "Content-Type: application/json" \
-d '{"name":"John Doe","email":"john.doe@example.com","dateOfBirth":"1990-01-01","phoneNumber":"1234567890"}'
Future Improvements
Add authentication (e.g., Spring Security).
Pagination for GET endpoints.
Integrate Swagger for API documentation.

This version is short, to the point, and covers the key information needed to use the project.

spring.datasource.url=jdbc:mysql://localhost:3306/registration_db
spring.datasource.username=your_username
spring.datasource.password=your_password
Run the application:

mvn spring-boot:run
Example Request: Create Registration
POST /api/registrations
Request Body:

{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "dateOfBirth": "1990-01-01",
  "phoneNumber": "1234567890"
}
Validation Rules
Name: Cannot be blank, max 100 characters.
Email: Must be valid and unique.
Date of Birth: Must be in the past.
Phone Number: Exactly 10 digits and unique.
Testing
Use Postman or cURL for testing. Example:

curl -X POST http://localhost:8080/api/registrations \
-H "Content-Type: application/json" \
-d '{"name":"John Doe","email":"john.doe@example.com","dateOfBirth":"1990-01-01","phoneNumber":"1234567890"}'
Future Improvements
Add authentication (e.g., Spring Security).
Pagination for GET endpoints.
Integrate Swagger for API documentation.

This version is short, to the point, and covers the key information needed to use the project.









