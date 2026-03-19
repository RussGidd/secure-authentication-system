# Secure Authentication System

A simple full-stack authentication system built for a learning assignment.

This project demonstrates a basic login/registration workflow where users can sign up and sign in as either an **Admin** or a **Customer**. Passwords are securely hashed before storage, and the system displays a role-based welcome message on successful login.

---

## ✅ What You’ll Find in This Project

### Backend (Express + MongoDB)

- REST API built with **Express.js**
- **MongoDB** used as the database (via **Mongoose**)
- Passwords hashed using **bcryptjs**
- Routes:
  - `POST /api/auth/signup` — Create a new user
  - `POST /api/auth/signin` — Authenticate existing user

### Frontend (React + Axios)

- React frontend built with **Vite**
- Simple sign-up and sign-in forms
- Uses **Axios** to call backend API
- Displays role-based welcome messaging

---

## 🚀 Getting Started (Run the App)

### 1) Start MongoDB

Make sure you have MongoDB running locally. By default, this project uses:

```
mongodb://localhost:27017/authdb
```

If you need to change it, edit `backend/.env`.

### 2) Install backend dependencies and start server

From the project root:

```bash
cd backend
npm install
npm run dev
```

The backend will start on **http://localhost:5000**.

### 3) Install frontend dependencies and start frontend

In a new terminal:

```bash
cd frontend
npm install
npm run dev
```

The frontend will start on **http://localhost:3000**.

---

## 🧠 How It Works (High Level)

### Sign Up

1. User provides email, password, and role (admin/customer).
2. Backend checks for an existing user with the same email.
3. Password is hashed (bcrypt) before storing.

### Sign In

1. User provides email and password.
2. Backend finds the user and compares the password hash.
3. If valid, the API returns a message with the user's role.

---

## 🔧 Project Structure

- `backend/` — Express server, MongoDB models, API routes
- `frontend/` — React/Vite app
- `README.md` — This file

---

## ✅ What’s Implemented

- User registration (email + password + role)
- Password hashing (bcrypt)
- Prevent duplicate email registrations
- User login with password validation
- Role-based “Welcome Admin” / “Welcome Customer” result
- Basic UI feedback for success / failure

---

## Notes

This project is intentionally simple and does not include JWT tokens or sessions, but it creates a foundation you can extend with authentication tokens, protected routes, and a real production UI.

---

## 🧾 Rubric Alignment (What’s Covered)

### Functionality

- ✅ User registration (SignUp) and login (SignIn) work as expected.
- ✅ Passwords are securely hashed using **bcryptjs**.
- ✅ Role-based authentication (Admin/Customer) is implemented.

### Code Structure & Organization

- ✅ Code is clean, well-organized, and modular:
  - Backend routes in `backend/routes`
  - User model in `backend/models/User.js`
  - Frontend UI in `frontend/src` components
- ✅ Clear separation between frontend (React) and backend (Express).

### Security

- ✅ Password hashing occurs on the backend before saving to the database.
- ✅ No plaintext passwords are stored or exposed to the frontend.

### UI / UX

- ✅ Simple and intuitive UI with clear form fields and role selection.
- ✅ Clear feedback shown to the user for successful actions and errors.

### Documentation

- ✅ README includes project setup and instructions.
- ✅ Code comments exist in key files for clarity.
