# Employee Manager

Employee Manager is a small full-stack practice project built with Angular, Spring Boot, and MySQL.

I created this project to practice how a frontend and backend work together in one application: building an Angular single-page app, exposing a Spring Boot REST API, and persisting data in MySQL.

The project started by following an Amigoscode full-stack Angular + Spring Boot tutorial. I then used that tutorial as a learning base and worked through the structure, CRUD flows, API communication, and local setup myself. This repository contains the matched frontend and backend version of that project in one place.

## Project Overview

The application simulates a simple employee administration system.

It includes:

- an Angular frontend in `employeemanager-angular/`
- a Spring Boot backend in the repository root
- MySQL as the database
- Docker files for local container-based running

Main functionality:

- view all employees
- add new employees
- update employee data
- delete employees
- search employees
- open an employee detail page
- manage salary entries for an employee

## Purpose Of The Project

This project was mainly a learning exercise.

I built it to practice:

- Angular components, routing, services, and forms
- Spring Boot controllers, services, and repositories
- REST API communication between frontend and backend
- CRUD operations across the full stack
- JPA entity mapping and MySQL persistence
- working with a larger project structure than a single small demo

It is not meant to be a large enterprise application. It is a compact practice project that helped me understand the basics of full-stack development with Java and Angular.

## What I Worked On

The project shows hands-on practice with:

- creating an employee overview page in Angular
- connecting Angular services to Spring Boot endpoints
- handling create, read, update, and delete flows
- building an employee detail page
- adding salary management connected to employees
- running the backend and frontend separately during development
- preparing the project for Docker-based local execution

## Technical Stack

### Frontend

- Angular 13
- TypeScript
- Angular Router
- Angular Forms
- RxJS
- Bootstrap 4
- Font Awesome

### Backend

- Spring Boot 2.7
- Spring Web
- Spring Data JPA
- Maven

### Database And Runtime

- MySQL
- Docker Compose
- Nginx for the production Angular build

## Application Structure

- `src/main/java`
  Spring Boot backend with controllers, services, repositories, and entities
- `src/main/resources/application.properties`
  backend configuration
- `employeemanager-angular/`
  Angular frontend
- `docker-compose.yml`
  local setup for frontend, backend, and MySQL
- `demo-screenshots/`
  screenshots of the application

## Main Features

### 1. Employee Overview

The home page loads employees from the backend and displays them as cards with basic profile information.

### 2. Employee CRUD

Employees can be added, edited, and deleted through the Angular UI, with the data stored through the Spring Boot API.

### 3. Employee Detail Page

Each employee has a dedicated detail page where profile data can be updated.

### 4. Salary Management

The project also includes a salary feature, where salary records can be added, updated, viewed, and deleted for a specific employee.

## Local Development

### Prerequisites

- Java and Maven
- Node.js and npm
- MySQL

### Backend

Create a MySQL database named:

`employeemanager`

Then set your local datasource values if needed:

```bash
export SPRING_DATASOURCE_URL=jdbc:mysql://localhost:3306/employeemanager
export SPRING_DATASOURCE_USERNAME=root
export SPRING_DATASOURCE_PASSWORD=your-password
```

Start the backend from the project root:

```bash
./mvnw spring-boot:run
```

The API runs on:

`http://localhost:8080`

### Frontend

Start the Angular app from `employeemanager-angular/`:

```bash
npm install
npm start
```

The frontend runs on:

`http://localhost:4200`

## Docker

The project also includes Docker support for running:

- MySQL
- Spring Boot backend
- Angular frontend

Run everything with:

```bash
docker compose up --build
```

Then open:

- frontend: `http://localhost:8081`
- backend: `http://localhost:8080`

## Tutorial Context

This project is based on an Amigoscode tutorial and was used as a personal practice project. I do not present it as an original product idea, but as a learning project that helped me understand Angular, Spring Boot, REST APIs, and full-stack application structure in a practical way.

## Author

Szilvia Varga
