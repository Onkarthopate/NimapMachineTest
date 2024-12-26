# NimapMachineTest

## To help you with the implementation of this Spring Boot project, here are the steps for each section

1. How did you run the code?
To run the Spring Boot project, follow these steps:
Clone the repository:
Clone the repository from GitHub or GitLab.
Use the command:
git clone : https://github.com/Onkarthopate/NimapMachineTest

Setup the project:
Open the project in your IDE (like IntelliJ or Eclipse).
Ensure that all dependencies are included in the pom.xml (for Maven).

Configure database:
Ensure the application.properties file is correctly set up for database configuration.
spring.datasource.url=jdbc:mysql://localhost:3306/db_name
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

Run the application:
In your IDE, run the Application class that has the @SpringBootApplication annotation.

2. How did you run the machine test?
The machine test can be executed as follows:
Use Postman or any API testing tool:
Open Postman or any other API client and test the API endpoints listed.
API Endpoints to Test:
GET http://localhost:8080/api/categories?page=3

POST http://localhost:8080/api/categories (For creating a new category)

GET http://localhost:8080/api/categories/{id} (For fetching category by id)

PUT http://localhost:8080/api/categories/{id} (For updating category by id)

DELETE http://localhost:8080/api/categories/{id} (For deleting category by id)

Repeat similar steps for the product CRUD operations.

Check Pagination:
Ensure that server-side pagination is working by specifying different page parameters in the GET
request.

Check One-to-Many Relationship:
For product endpoints, the category details should be included in the product response.

3. DB Design
For the one-to-many relationship between Category and Product, your DB design will include two
tables:

Category Table:
sql
CREATE TABLE category (
id BIGINT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(255) NOT NULL
);

Product Table:
sql
CREATE TABLE product (
id BIGINT AUTO_INCREMENT PRIMARY KEY,
name VARCHAR(255) NOT NULL,
category_id BIGINT,
FOREIGN KEY (category_id) REFERENCES category(id) );

Note: The category_id field in the product table represents the foreign key to the category table,
establishing a one-to-many relationship.
