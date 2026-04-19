BrainWave – Role-Based Task & Assignment Management System

Project Overview

BrainWave is a full-stack Java web application built with Spring Boot, designed to simplify academic organization for students, teachers, and administrators. The platform provides a clean and structured environment where users can manage tasks, assignments, and academic progress through a secure role-based system.

The application was created to solve common problems students face with disorganized coursework, scattered deadlines, and poor visibility of responsibilities. By combining authentication, role-based access control, task tracking, and assignment management into one platform, BrainWave delivers a simpler and more efficient learning experience.

Core Features

User Authentication

Secure user registration

Secure login system

Password encryption using Spring Security

Session management

Role-based page access

Role-Based Authorization

The system supports three domain-specific roles:

Admin

Full administrative access

Manage users

View registered accounts

Access Admin Dashboard

Manage assignments and tasks

View system statistics

Teacher

Create assignments

View assignments

Delete assignments they created

Manage academic content

Student

Create personal tasks

Edit their own tasks

Delete their own tasks

View assignments

Track coursework and deadlines

Search & Filtering System

BrainWave includes an advanced assignment management system with search and filtering options.

Users can filter assignments by:

Status

Priority

Sort order

Title search

This improves efficiency and allows quick access to important tasks and assignments.

Technology Stack

Backend

Java

Spring Boot

Spring MVC

Spring Security

Spring Data JPA

Hibernate

Frontend

Thymeleaf

HTML5

CSS3

Bootstrap

Database

H2 Database

JPA Repository Layer

Tools & Deployment

Maven

Docker

GitHub

VS Code

IntelliJ IDEA

How to Run the Project

Option 1 – Run in VS Code / IntelliJ

Requirements

Java 17 or higher

Maven installed

Git installed

Clone Repository

git clone https://github.com/SolomonOzorSectionE/Web-Application-Development---CPAN-228-Final-project.git
cd Web-Application-Development---CPAN-228-Final-project

Run Application

For Windows:

.\mvnw.cmd spring-boot:run

For Mac / Linux:

./mvnw spring-boot:run

Open Browser

http://localhost:8080

Run Using Docker

Build Docker Image

docker build -t brainwave-app .

Run Docker Container

docker run -p 8080:8080 brainwave-app

Open Browser

http://localhost:8080

Required Setup / Environment Variables

The project uses an H2 in-memory database in development mode, so no external database installation is required.

spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.username=sa
spring.datasource.password=
spring.h2.console.enabled=true
server.port=8080
spring.profiles.active=dev

All settings can be modified in src/main/resources/application.properties.

Application Routes

Route

Description

/

Home Page

/about

About Page

/features

Features Page

/register

Register New User

/login

User Login

/assignments

View Assignments

/task/create

Create Task

/tasks

My Tasks

/admin

Admin Dashboard

/h2-console

Database Console

Project Structure

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

Team Contributions

Solomon

Configured database connection and persistence layer

Implemented domain-specific roles (Admin, Teacher, Student)

Built Admin Dashboard and admin interface

Managed repository structure, commits, branches, and collaboration workflow

Ashton

Developed the original navigation system between pages

Built user management features

Implemented user registration functionality

Helped establish early project structure

Ahmad

Created startup sample data

Improved presentation and styling using Bootstrap

Built login pages and route flow

Configured Docker support

Created H2 development profile

Produced the main presentation video

Karn

Built search functionality

Developed list/display functions

Assisted with assignment filtering features

Produced the second presentation video

Team Collaboration

Although each member had assigned responsibilities, the team worked together throughout the development process.

The entire team contributed to:

Debugging application issues

Improving UI design

Fixing styling inconsistencies

Correcting route errors

Resolving logic bugs

Refining page layouts

Improving usability

Fixing small code errors collaboratively

The final application reflects strong teamwork, communication, and shared problem-solving.

Sample Data on Startup

The application includes startup sample data to make testing and demonstration easier. Users can immediately explore the system after launching the project without manually entering records.


