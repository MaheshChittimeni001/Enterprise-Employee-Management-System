# 🏢 Enterprise Employee Management System

A full-stack **Enterprise Employee Management System** built using **Java, Spring Boot, Spring Data JPA, React.js, and MySQL**. The application provides a responsive interface for managing employee records with complete **CRUD operations**, RESTful API integration, form validation, and client-side routing.

The project follows a **layered backend architecture** using Spring MVC and Spring Data JPA to provide clean separation of concerns, maintainability, and efficient data persistence.

---

## 🚀 Features

### 👨‍💼 Employee Management

* Create new employee records
* View all employees
* View employee details
* Update employee information
* Delete employee records
* Complete CRUD functionality

### 🎨 Frontend

* Responsive and user-friendly UI
* React.js component-based architecture
* Client-side routing using React Router
* Form validation
* REST API integration
* Dynamic employee data rendering
* Navigation between application pages

### ⚙️ Backend

* RESTful API development using Spring Boot
* Spring MVC architecture
* Layered architecture
* Spring Data JPA for database operations
* Hibernate ORM
* MySQL database integration
* Exception handling
* Clean separation between Controller, Service, and Repository layers

---

## 🛠️ Tech Stack

| Technology          | Purpose                        |
| ------------------- | ------------------------------ |
| **Java**            | Backend programming language   |
| **Spring Boot**     | Backend application framework  |
| **Spring MVC**      | Web and REST API layer         |
| **Spring Data JPA** | Database interaction           |
| **Hibernate**       | ORM framework                  |
| **RESTful APIs**    | Frontend-backend communication |
| **React.js**        | Frontend development           |
| **React Router**    | Client-side routing            |
| **MySQL**           | Relational database            |
| **HTML5 / CSS3**    | UI structure and styling       |
| **Git & GitHub**    | Version control                |

---

## 🏗️ Project Architecture

The backend follows a layered architecture:

```text
                    ┌──────────────────────┐
                    │      React.js        │
                    │   Frontend / UI      │
                    └──────────┬───────────┘
                               │
                               │ REST API
                               ▼
                    ┌──────────────────────┐
                    │    Controller Layer  │
                    │    Spring MVC        │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │     Service Layer    │
                    │   Business Logic     │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   Repository Layer   │
                    │ Spring Data JPA      │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │      MySQL           │
                    │      Database        │
                    └──────────────────────┘
```

### Backend Structure

```text
src/main/java/
└── com.example.employeemanagement
    ├── controller
    │   └── EmployeeController.java
    │
    ├── service
    │   └── EmployeeService.java
    │
    ├── repository
    │   └── EmployeeRepository.java
    │
    ├── entity
    │   └── Employee.java
    │
    └── EmployeeManagementApplication.java
```

### Frontend Structure

```text
react-frontend/
└── src/
    ├── components/
    │   ├── EmployeeList.js
    │   ├── CreateEmployee.js
    │   ├── UpdateEmployee.js
    │   └── ViewEmployee.js
    │
    ├── services/
    │   └── EmployeeService.js
    │
    ├── App.js
    └── index.js
```

---

## 🔄 Application Workflow

```text
User
 │
 ▼
React.js UI
 │
 │ HTTP Request
 ▼
Spring Boot REST API
 │
 ▼
Controller
 │
 ▼
Service
 │
 ▼
Spring Data JPA
 │
 ▼
Hibernate
 │
 ▼
MySQL Database
 │
 └──────────────► Response
                       │
                       ▼
                  React.js UI
```

---

## 📌 REST API Endpoints

| Method   | Endpoint              | Description           |
| -------- | --------------------- | --------------------- |
| `GET`    | `/api/employees`      | Get all employees     |
| `GET`    | `/api/employees/{id}` | Get employee by ID    |
| `POST`   | `/api/employees`      | Create a new employee |
| `PUT`    | `/api/employees/{id}` | Update employee       |
| `DELETE` | `/api/employees/{id}` | Delete employee       |

### Example Employee JSON

```json
{
  "firstName": "Mahesh",
  "lastName": "Chittimeni",
  "emailId": "mahesh@example.com"
}
```

---

# 💻 Getting Started

## Prerequisites

Make sure the following are installed:

* Java JDK 17 or later
* Maven
* Node.js
* npm
* MySQL
* Git

---

## 🗄️ Database Setup

Create the MySQL database:

```sql
CREATE DATABASE employee_management_system;
```

Update your Spring Boot `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/employee_management_system?useSSL=false
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect

server.port=8080
```

> Replace `YOUR_PASSWORD` with your local MySQL password.

---

# ⚙️ Running the Backend

Navigate to the Spring Boot project:

```bash
cd backend
```

Run the application using Maven:

```bash
mvn spring-boot:run
```

The backend will start at:

```text
http://localhost:8080
```

---

# 🎨 Running the Frontend

Open another terminal and navigate to the React project:

```bash
cd react-frontend
```

Install dependencies:

```bash
npm install
```

Start the React application:

```bash
npm start
```

The frontend will be available at:

```text
http://localhost:3000
```

---

# 📸 Application Screens

Add your project screenshots here:

```text
screenshots/
├── employee-list.png
├── add-employee.png
├── update-employee.png
└── view-employee.png
```

Example:

```markdown
## 📸 Screenshots

### Employee List
![Employee List](screenshots/employee-list.png)

### Add Employee
![Add Employee](screenshots/add-employee.png)

### Update Employee
![Update Employee](screenshots/update-employee.png)
```

---

# 🧪 CRUD Operations

### Create

Users can add a new employee by submitting the employee form.

```http
POST /api/employees
```

### Read

Employee records can be retrieved from the database.

```http
GET /api/employees
```

### Update

Existing employee information can be modified.

```http
PUT /api/employees/{id}
```

### Delete

Employee records can be removed from the system.

```http
DELETE /api/employees/{id}
```

---

# 🔐 Validation & Error Handling

The application implements:

* Client-side form validation
* Required field validation
* Email validation
* REST API error handling
* Backend exception handling
* Database constraint handling

---

# 📚 Key Concepts Demonstrated

This project demonstrates practical knowledge of:

* Core Java
* Object-Oriented Programming
* Spring Boot
* Spring MVC
* RESTful Web Services
* Spring Data JPA
* Hibernate
* MySQL
* React.js
* React Router
* HTTP methods
* CRUD operations
* Frontend-backend integration
* Layered architecture
* MVC architecture
* Database persistence
* Git & GitHub

---

# 🎯 Learning Outcomes

Through this project, I gained hands-on experience in designing and developing a complete full-stack web application.

Key learning outcomes include:

* Building REST APIs using Spring Boot
* Implementing CRUD operations with Spring Data JPA
* Connecting Spring Boot applications with MySQL
* Developing reusable React components
* Integrating React.js with REST APIs
* Implementing client-side routing
* Handling form validation
* Understanding layered backend architecture
* Managing frontend and backend communication
* Using Git and GitHub for version control

---

# 🔮 Future Enhancements

The project can be further enhanced with:

* 🔐 Spring Security and JWT authentication
* 👥 Role-based access control
* 🔎 Employee search and filtering
* 📄 Pagination and sorting
* 📊 Employee dashboard and analytics
* 📧 Email notifications
* 🐳 Docker containerization
* ☁️ Cloud deployment
* 🧪 Unit and integration testing

---

# 👨‍💻 Author

**Mahesh Chittimeni**

**Software Engineer | Backend Developer**

* Java
* Spring Boot
* REST APIs
* React.js
* MySQL
* Data Structures & Algorithms

---

## ⭐ Support

If you found this project useful, consider giving the repository a ⭐ on GitHub!

---

## 📄 License

This project is created for educational and portfolio purposes.
