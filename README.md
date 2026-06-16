# Employee Leave Management System

A Flask-based application for managing employee leave requests.

## Setup Instructions

1. **Navigate to the project directory**:
   ```bash
   cd d:\MiniProject\Employee_Leave_Management
   ```

2. **Install dependencies** (in your virtual environment):
   ```bash
   ..\.venv\Scripts\pip.exe install -r requirements.txt
   ```

3. **Initialize the database and seed the admin**:
   Run the application, then visit the following routes in your web browser:
   *   Initialize DB: `http://localhost:5000/init_db`
   *   Seed Admin: `http://localhost:5000/seed_admin`

4. **Run the application**:
   ```bash
   ..\.venv\Scripts\python.exe app.py
   ```

5. **Access the Application**:
   Open **http://localhost:5000** in your browser.

## Features
- User registration and login
- Leave application
- Leave history tracking
- Admin dashboard for managing requests
- Modern, clean, responsive design using custom CSS macros

