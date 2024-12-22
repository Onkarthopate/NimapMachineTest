# NimapMachineTest
## Category-Product Management System
### Overview
This is a Spring Boot application for managing Categories and Products with REST APIs. It supports full CRUD operations (Create, Read, Update, Delete) for both entities and maintains a one-to-many relationship between Categories and Products. The project includes pagination for fetching records and uses Spring Data JPA for database interaction.

### Features
CRUD Operations:

Categories: Create, Read, Update, Delete. Products: Create, Read, Update, Delete. One-to-Many Relationship:

A single category can have multiple products.
Pagination:

Paginated retrieval for both categories and products. Database Integration:

Uses MySQL (or any other RDBMS) as the database. Annotation-based Configuration:

Fully configured using Java annotations (no XML).

### RESTful APIs:
Developed using Spring Boot's REST Controller.
Tech Stack Backend Framework: Spring Boot Database: MySQL (or any RDBMS with JPA support) Build Tool: Maven ORM Framework: Hibernate with JPA Java Version: Java 11 or later

### Prerequisites
Java 11 or above installed. MySQL installed and running. Postman (or any API testing tool) for testing the APIs.

