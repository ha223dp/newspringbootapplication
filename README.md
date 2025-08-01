#Newspringbootapplication
A simple Spring Boot application created to explore and practice core backend development concepts including API creation, testing with Postman, and integration with a MySQL database.

Overview
This project was developed as part of my learning journey with Spring Boot. The main goal was to understand how to:

Set up a RESTful API with Spring Boot

Connect the application to a MySQL database

Perform CRUD operations

Test endpoints using Postman

Technologies Used
Java 17

Spring Boot 

Spring Security

Spring Data JPA

MySQL

Postman (for testing)

Maven

-Features
RESTful API with basic CRUD operations

MySQL database integration using Spring Data JPA

API tested with Postman

Simple and clean architecture for easy understanding

Setup Instructions
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/yourusername/newspringbootapplication.git
cd newspringbootapplication
2. Configure MySQL Database
Create a database named dream_shops_db and update application.properties:

properties
Copy
Edit

spring.application.name=dream-shops

server.port=9191

spring.datasource.url=jdbc:mysql://localhost:3306/dream_shops_db
spring.datasource.username=<your username>
spring.datasource.password=<your password>

spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQLDialect

spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
##(create, update, create-drop, validate)
spring.jpa.hibernate.ddl-auto=update

spring.servlet.multipart.max-file-size=5MB
spring.servlet.multipart.max-request-size=5MB


api.prefix=/api/v1
auth.token.jwtSecret=
auth.token.expirationInMils=86400000

3. Build and Run the Application
bash
Copy
Edit
./mvnw spring-boot:run
Or from your IDE (e.g., IntelliJ or Eclipse), run the DreamShopsApplication class.

4. Test with Postman
You can test the API endpoints using Postman. Example endpoints:

http://localhost:9191/api/v1/products/all

Make sure to set the Content-Type to application/json when sending requests.

What I Learned
Setting up and structuring a Spring Boot project

Using Spring Data JPA for seamless database operations

How to connect Spring Boot with MySQL

API testing with Postman

Best practices for backend development

Future Improvements
Add authentication (e.g., Spring Security + JWT)

Input validation and error handling

Swagger UI for API documentation


Contributing
Feel free to fork this repo and suggest improvements or features. Contributions are welcome!

License
This project is open source and available under the MIT License.
