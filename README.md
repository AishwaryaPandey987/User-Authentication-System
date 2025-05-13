# User Authentication System

This is a simple User Authentication System built using **Spring Boot**, **Maven**, **Java**, and **MySQL**. The project allows users to register, log in, and securely store their credentials (email and password) in a MySQL database.

## Features

- **User Registration**: Allows users to create an account by providing an email and password.
- **User Login**: Users can log in using their credentials.
- **Password Storage**: Passwords are securely stored in MySQL using hashing algorithms.
- **Basic Validation**: Ensures users input valid email addresses and strong passwords.

## Technologies Used

- **Backend**: Spring Boot
- **Database**: MySQL
- **Build Tool**: Maven
- **Java Version**: Java 8 or higher
- **Security**: Password hashing using BCrypt

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Java 8 or higher installed on your machine.
- Maven installed for building the project.
- MySQL installed and running.
- A MySQL database for storing user data.

## Setup and Installation

### 1. Clone the Repository

Clone the repository to your local machine using Git:

```bash
git clone https://github.com/AishwaryaPandey987/User-Authentication-System.git

2. Configure MySQL Database
Create a database in MySQL for storing user credentials:

sql
Copy
Edit
CREATE DATABASE user_authentication;

Configure the application.properties file (located at src/main/resources/application.properties) to use your MySQL credentials:

spring.datasource.url=jdbc:mysql://localhost:3306/user_authentication
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD
spring.jpa.hibernate.ddl-auto=update
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
3. Build the Project
Navigate to the project folder and run Maven to build the project:

bash
Copy
Edit
mvn clean install
4. Run the Application
You can now run the application:

bash
Copy
Edit
mvn spring-boot:run
The application should start and be available at http://localhost:8080.

Endpoints
POST /api/register - Registers a new user.

Request body: { "email": "user@example.com", "password": "securepassword" }

POST /api/login - Logs in an existing user.

Request body: { "email": "user@example.com", "password": "securepassword" }

Database Schema
The project uses the following MySQL table structure:

sql
Copy
Edit
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);
Security
Passwords are securely stored using BCrypt hashing for improved security. When users register or log in, their passwords are hashed and compared against the stored hash.

Contributions
Contributions are welcome! If you'd like to contribute to this project, please fork the repository and submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

yaml
Copy
Edit

---

### Key Sections:
1. **Overview**: Describes the purpose of the project.
2. **Technologies Used**: Lists the tech stack.
3. **Installation**: Provides step-by-step instructions on how to clone, set up, and run the project.
4. **Endpoints**: Describes the key REST API endpoints.
5. **Database Schema**: Shows the MySQL table structure.
6. **Security**: Mentions how passwords are securely handled.
7. **Contributions**: Encourages others to contribute.

---

Feel free to adjust the instructions if your project has specific needs! Let me know if you need a
