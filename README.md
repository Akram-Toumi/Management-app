# Project Management Application

## Introduction

Efficient management of projects and tasks is crucial for productivity. Existing tools are often too complex or lack specific features. This application aims to provide a user-friendly solution for managing projects and tasks effectively.

## Features

1. **User Authentication**: Secure login and registration.
2. **Project Management**: Create, update, delete, and view projects.
3. **Task Management**: Add, update, delete, and view tasks within projects.
4. **Data Persistence**: Robust storage using PostgreSQL for reliability and scalability.

## Technologies Used

- **NestJS**: Framework for creating efficient and modular server-side applications.
- **PostgreSQL**: Relational database for structured storage.
- **ReactJS**: JavaScript library for building an interactive and responsive user interface.
- **Additional Tools**:
  - **TypeORM**: Database interaction.
  - **Docker**: Containerized deployment (if applicable).
  - **GitHub**: Source code management and collaboration.
  - **Postman**: API testing and documentation.

## System Architecture

- **Frontend**: Built with ReactJS for an intuitive user interface.
- **Backend**: API built with NestJS, handling business logic, authentication, and data validation.
- **Database**: PostgreSQL stores users, projects, and tasks.

Key Features:
- RESTful APIs for seamless integration.
- Secure authentication with JWT or OAuth2.

## Database Schema

- **Tables**:
  - `Users`: `userID`, `username`, `email`, `password`.
  - `Projects`: `projectID`, `projectName`, `description`, `userID` (foreign key).
  - `Tasks`: `taskID`, `taskName`, `deadline`, `status`, `projectID` (foreign key).
- **Relationships**:
  - One-to-Many: Users → Projects.
  - One-to-Many: Projects → Tasks.

## Key API Endpoints

### User Routes
- `POST /auth/signup`: Create an account.
- `POST /auth/login`: Authenticate a user.

### Project Routes
- `POST /projects`: Add a new project.
- `PATCH /projects/:id`: Update a project.
- `DELETE /projects/:id`: Delete a project.

### Task Routes
- `POST /projects/:projectId/tasks`: Add a task.
- `PATCH /tasks/:taskId`: Update a task.
- `DELETE /tasks/:taskId`: Delete a task.

## Demonstration

- User authentication process.
- Adding, updating, and deleting a project.
- Managing tasks within a project.

## Challenges and Solutions

### Challenges
- Integrating secure authentication.
- Optimizing database queries for scalability.

### Solutions
- Leveraging NestJS's built-in security features.
- Designing a normalized database schema for efficiency.

## Future Improvements

- Implement a frontend interface (e.g., React or Angular).
- Add notifications or reminders for task deadlines.
- Integrate analytics for project progress tracking.
- Enable team collaboration features.

## Conclusion

This project offers an efficient and secure solution for project and task management, with a modular design for future scalability.

---
*Developed by Barkia Firas and Toumi Akram.*
