# Attendance Management System

## Features
- JWT Login and role management: Admin, Teacher, Student
- Class/section/year management
- Subject management with teacher and class assignment
- Bulk daily attendance marking
- Automatic attendance percentage calculation
- Attendance report for admin/teacher and personal report for students
- Responsive HTML/CSS/JavaScript frontend
- Node.js + Express + MongoDB/Mongoose backend

## Requirements
- Node.js 18+
- MongoDB local or MongoDB Atlas

## Run
1. Extract the ZIP.
2. Open the project folder in VS Code.
3. Run `npm install`.
4. Copy `.env.example` to `.env` and set `MONGO_URI` and `JWT_SECRET`.
5. Run `npm start`.
6. Open `http://localhost:5000`.

## Demo accounts
- Admin: admin@example.com / admin123
- Teacher: teacher@example.com / teacher123
- Student: student@example.com / student123

On the first run, demo users, one BCA class and one subject are automatically created if the database is empty.
