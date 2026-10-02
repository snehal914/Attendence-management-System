Attendance Management System

A full-stack web application for managing students, teachers, classes, subjects, attendance, attendance percentage, and attendance reports.

Technologies Used

Frontend

- HTML5
- CSS3
- JavaScript

Backend

- Node.js
- Express.js
- JWT Authentication
- bcryptjs

Database

- MongoDB
- Mongoose

---

Features

1. Login and Role Management

The system provides secure login functionality with three different roles:

- Admin
  
  - Manage users
  - Manage classes
  - Manage subjects
  - View attendance reports

- Teacher
  
  - View assigned classes and subjects
  - Mark student attendance
  - View attendance reports

- Student
  
  - View personal attendance
  - View attendance percentage
  - View attendance report

---

2. Class/Subject Management

Admin can manage:

- Classes
- Sections
- Subjects
- Teachers
- Students

Each subject can be assigned to a particular class and teacher.

---

3. Mark Attendance

Teachers can mark attendance for students.

Attendance status can be:

- Present
- Absent

The teacher selects:

1. Class
2. Subject
3. Date
4. Student
5. Attendance status

The attendance is then stored in MongoDB.

---

4. Attendance Percentage

The system automatically calculates attendance percentage.

Formula

Attendance Percentage =
(Present Classes / Total Classes) × 100

Example

If a student attended 8 classes out of 10:

(8 / 10) × 100 = 80%

Therefore, the student's attendance percentage is 80%.

---

5. Attendance Report

The system provides attendance reports containing:

- Student name
- Class
- Subject
- Total classes
- Present classes
- Absent classes
- Attendance percentage

Students can view their own attendance, while teachers and admins can view reports according to their permissions.

---

Project Structure

attendance-management-system/
│
├── server.js
├── package.json
├── .env.example
├── README.md
│
├── config/
│   └── db.js
│
├── middleware/
│   └── auth.js
│
├── models/
│   ├── User.js
│   ├── Class.js
│   ├── Subject.js
│   └── Attendance.js
│
├── routes/
│   ├── auth.js
│   ├── users.js
│   ├── classes.js
│   ├── subjects.js
│   └── attendance.js
│
└── public/
    ├── index.html
    ├── dashboard.html
    ├── attendance.html
    ├── report.html
    │
    ├── css/
    │   └── style.css
    │
    └── js/
        ├── login.js
        ├── dashboard.js
        ├── attendance.js
        └── report.js

---

Requirements

Before running the project, install:

- Node.js
- MongoDB or MongoDB Atlas
- Visual Studio Code
- Web browser

---

Installation

Step 1: Extract the Project

Extract the ZIP file.

Open the project folder in Visual Studio Code.

---

Step 2: Open Terminal

In VS Code, open:

Terminal → New Terminal

---

Step 3: Install Dependencies

Run:

npm install

---

Step 4: Configure MongoDB

Create a MongoDB database using:

- Local MongoDB

or

- MongoDB Atlas

Copy your MongoDB connection string.

---

Step 5: Create ".env"

Create a file named:

.env

Add:

PORT=5000
MONGO_URI=mongodb://127.0.0.1:27017/attendance_management
JWT_SECRET=myattendance_secret_key

For MongoDB Atlas, replace "MONGO_URI" with your Atlas connection string.

---

Running the Project

Start the server using:

npm start

or:

node server.js

You should see:

Server running on port 5000
MongoDB connected

Open your browser and visit:

http://localhost:5000

---

Demo Login

Admin

Email: admin@example.com
Password: admin123
Role: Admin

Teacher

Email: teacher@example.com
Password: teacher123
Role: Teacher

Student

Email: student@example.com
Password: student123
Role: Student

«If these accounts are not automatically created by your version of the project, create them through the user-registration/seed functionality provided in the project.»

---

Application Workflow

Login
  ↓
Role Verification
  ↓
Dashboard
  ↓
Select Class
  ↓
Select Subject
  ↓
Select Date
  ↓
Mark Attendance
  ↓
Save Attendance
  ↓
Calculate Percentage
  ↓
Generate Attendance Report

---

Attendance Calculation

For example:

Total Classes = 20
Present = 17
Absent = 3

Calculation:

(17 / 20) × 100
= 85%

Attendance percentage:

85%

---

Security

The application uses:

- Password hashing using "bcryptjs"
- JWT-based authentication
- Role-based authorization
- Protected API routes
- Environment variables for sensitive configuration

Do not upload your ".env" file to GitHub because it may contain database credentials and secret keys.

---

API Overview

Authentication

Login

POST /api/auth/login

Register

POST /api/auth/register

---

Classes

GET /api/classes
POST /api/classes
PUT /api/classes/:id
DELETE /api/classes/:id

---

Subjects

GET /api/subjects
POST /api/subjects
PUT /api/subjects/:id
DELETE /api/subjects/:id

---

Attendance

POST /api/attendance
GET /api/attendance
GET /api/attendance/report

---

Future Enhancements

The following features can be added later:

- 📧 Email notifications
- 📱 Mobile application
- 📄 PDF attendance reports
- 📊 Graphs and charts
- 📥 Excel report download
- 🔔 Low-attendance notifications
- 📅 Monthly attendance reports
- 🗓️ Attendance calendar
- 👨‍👩‍👧 Parent login
- ☁️ Cloud deployment

---

Author

Attendance Management System

Developed as a full-stack web application project for managing student attendance efficiently.
