# BrainWave – Role-Based Task & Assignment Management System

## Project Overview

BrainWave is a full-stack Java web application built with Spring Boot to simplify academic organization for students, teachers, and administrators. The platform provides a clean and structured environment where users can manage tasks, assignments, and academic progress through a secure role-based system.

The application was created to address common student challenges such as disorganized coursework, scattered deadlines, and poor visibility of responsibilities. By combining authentication, role-based access control, task tracking, and assignment management into one platform, BrainWave provides a simpler and more efficient learning experience.

## Core Features

### User Authentication
- Secure user registration
- Secure login system
- Password encryption using Spring Security
- Session management
- Role-based page access

### Role-Based Authorization

The system supports three domain-specific roles:

#### Admin
- Full administrative access
- Manage users
- View registered accounts
- Access the Admin Dashboard
- Manage assignments and tasks
- View system statistics

#### Teacher
- Create assignments
- View assignments
- Delete assignments they created
- Manage academic content

#### Student
- Create personal tasks
- Edit their own tasks
- Delete their own tasks
- View assignments
- Track coursework and deadlines

### Search and Filtering System

BrainWave includes an assignment management system with search and filtering options.

Users can filter assignments by:
- Status
- Priority
- Sort order
- Title search

This improves efficiency and allows quick access to important tasks and assignments.

## Technology Stack

### Backend
- Java
- Spring Boot
- Spring MVC
- Spring Security
- Spring Data JPA
- Hibernate

### Frontend
- Thymeleaf
- HTML5
- CSS3
- Bootstrap

### Database
- H2 Database
- JPA Repository Layer

### Tools and Deployment
- Maven
- Docker
- GitHub
- VS Code
- IntelliJ IDEA

## How to Run the Project

### Option 1: Run in VS Code or IntelliJ

#### Requirements
- Java 17 or higher
- Maven installed
- Git installed

#### Clone the Repository

```bash
git clone https://github.com/SolomonOzorSectionE/Web-Application-Development---CPAN-228-Final-project.git
cd Web-Application-Development---CPAN-228-Final-project
```

#### Run the Application

**Windows**
```bash
.\mvnw.cmd spring-boot:run
```

**Mac/Linux**
```bash
./mvnw spring-boot:run
```

#### Open the Application
http://localhost:8080

### Run Using Docker

#### Build the Docker Image
```bash
docker build -t brainwave-app .
```

#### Run the Docker Container
```bash
docker run -p 8080:8080 brainwave-app
```

#### Open the Application
http://localhost:8080

## Required Setup and Environment Variables

The project uses an H2 in-memory database in development mode, so no external database installation is required.

Default configuration:

```properties
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=
spring.h2.console.enabled=true
server.port=8080
spring.profiles.active=dev
```

All settings can be modified in:

```text
src/main/resources/application.properties
```

## Application Routes

| Route | Description |
|---|---|
| / | Home Page |
| /about | About Page |
| /features | Features Page |
| /register | Register New User |
| /login | User Login |
| /assignments | View Assignments |
| /task/create | Create Task |
| /tasks | My Tasks |
| /admin | Admin Dashboard |
| /h2-console | Database Console |

## Project Structure

```text
src/
└── main/
    ├── java/
    │   └── com/brainwave/app/
    ├── resources/
    │   ├── templates/
    │   ├── static/
    │   └── application.properties

pom.xml
Dockerfile
README.md
```

## Team Contributions

### Solomon
- Configured the database connection and persistence layer
- Implemented domain-specific roles: Admin, Teacher, and Student
- Built the Admin Dashboard and admin interface
- Managed the repository structure, commits, branches, and collaboration workflow

### Ashton
- Developed the original navigation system between pages
- Built user management features
- Implemented user registration functionality
- Helped establish the early project structure

### Ahmad
- Created startup sample data
- Improved presentation and styling using Bootstrap
- Built the login pages and route flow
- Configured Docker support
- Created the H2 development profile
- Produced the main presentation video

### Karn
- Built the search functionality
- Developed list and display functions
- Assisted with assignment filtering features
- Produced the second presentation video

## Team Collaboration

The entire team contributed to:
- Debugging application issues
- Improving UI design
- Fixing styling inconsistencies
- Correcting route errors
- Resolving logic bugs
- Refining page layouts
- Improving usability
- Fixing small code errors collaboratively

The final application reflects strong teamwork, communication, and shared problem-solving.


## Conclusion

BrainWave demonstrates real-world full-stack development concepts including authentication, authorization, CRUD operations, search systems, database integration, Docker deployment, and collaborative software development.

The project provides a practical academic productivity solution while showcasing modern Java web development best practices.
