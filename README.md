# Student Management System

A simple Express.js and MySQL student management web application for adding, viewing, and searching student records.

## Features
- Add new students
- View all students in a table
- Search students by student ID, first name, last name, or course
- Uses EJS templates for the UI

## Project Structure
- `app.js` — Express server and database logic
- `views/` — EJS templates
  - `index.ejs` — student list page
  - `add.ejs` — add student form
- `public/` — static assets

## Requirements
- Node.js
- MySQL
- npm

## Setup
1. Install dependencies:
   ```bash
   npm install
   ```

2. Make sure MySQL is running locally.

3. Create a database named `student_management`.

4. Create a `students` table with a structure similar to:
   ```sql
   CREATE TABLE students (
     id INT AUTO_INCREMENT PRIMARY KEY,
     student_id VARCHAR(50) NOT NULL,
     first_name VARCHAR(100) NOT NULL,
     last_name VARCHAR(100) NOT NULL,
     course VARCHAR(100) NOT NULL,
     year_level INT NOT NULL,
     email VARCHAR(150) NOT NULL
   );
   ```

5. Start the app:
   ```bash
   node app.js
   ```

6. Open in the browser:
   ```text
   http://localhost:3000
   ```

## Environment
The app uses MySQL on `127.0.0.1:3306` by default. If needed, you can override the port using:
```bash
DB_PORT=3306 node app.js
```

## Notes
- Ensure your MySQL user credentials match your local database setup.
- The application currently uses the root user with password `root` for local development.
