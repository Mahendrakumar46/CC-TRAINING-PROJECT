# Complete Smart Attendance System

This is the final, comprehensive version of the Smart Attendance System implemented in Java (Spring Boot) and MySQL.

## Features
- **Security:** Spring Security + JWT authentication. Passwords hashed using BCrypt.
- **Roles:** Unified login for both `ADMIN` and `STUDENT` roles with automatic redirection.
- **Student Dashboard:** View/Edit profile, enter present/absent days, auto-calculate metrics safely.
- **Admin Dashboard:** View all students, search by keyword, filter by course/department, and automatically highlight students with < 75% attendance in red.
- **Architecture:** MVC (Model-View-Controller) pattern with strict layering (Controller, Service, Repository, Entity, DTO, Security, Config, Exception).
- **Global Error Handling:** Friendly, structured JSON error responses via `@ControllerAdvice`.

## Setup Instructions

### 1. Database
Run the provided `schema.sql` script in your MySQL workbench or terminal. It automatically creates the database `smart_attendance_complete`, tables, and default users.

### 2. Application Configuration
Ensure your MySQL credentials (`root`/`root`) are correct in `src/main/resources/application.properties`.

### 3. Run Application
From the root folder `d:/smart attendance`, execute:
```bash
mvn clean install -DskipTests
mvn spring-boot:run
```

### 4. Access the Application
Open your browser to: `http://localhost:8080/`

**Test Accounts:**
- Admin: `admin@system.com` / `admin123`
- Student: `student@school.com` / `student123`
