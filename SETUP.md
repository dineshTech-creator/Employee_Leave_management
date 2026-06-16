# Employee Leave Management System - Setup & Run Guide

## ✅ Quick Start (SQLite - No Server Needed!)

This project now uses **SQLite** instead of MySQL, making it super easy to run locally with zero configuration!

### Step 1: Install Dependencies
```bash
cd d:\MiniProject\Employee_Leave_Management
pip install -r requirements.txt
```

### Step 2: Initialize Database
Open your browser and visit:
```
http://localhost:5000/init_db
```
You should see: ✅ Database initialized!

### Step 3: Create Admin Account
Visit:
```
http://localhost:5000/seed_admin
```
You should see: ✅ Admin created! Email: admin@company.com | Password: Admin@123

### Step 4: Run the Application
```bash
python app.py
```

You should see:
```
 * Running on http://127.0.0.1:5000
 * Press CTRL+C to quit
```

### Step 5: Open in Browser
Go to: **http://localhost:5000**

---

## 🎯 Default Credentials

**Admin Login:**
- Email: `admin@company.com`
- Password: `Admin@123`

**Employee:**
- Register a new account to test employee features

---

## 📁 Project Structure

```
Employee_Leave_Management/
├── app.py                      # Flask app with SQLAlchemy
├── leave_management.db         # SQLite database (created automatically)
├── requirements.txt            # Python dependencies
├── README.md                   # This file
│
├── templates/
│   ├── index.html              # Landing page
│   ├── employee_login.html     # Employee login
│   ├── employee_register.html  # Employee registration
│   ├── employee_dashboard.html # Employee dashboard
│   ├── apply_leave.html        # Leave application form
│   ├── leave_history.html      # Leave history
│   ├── employee_profile.html   # Employee profile
│   ├── admin_login.html        # Admin login
│   ├── admin_dashboard.html    # Admin dashboard
│   ├── admin_leave_requests.html # Manage leave requests
│   ├── admin_employees.html    # Manage employees
│   ├── admin_employee_detail.html # Employee details
│   └── base.html               # Base template
│
└── static/
    ├── css/
    │   └── style.css           # Styling
    └── js/
        └── script.js           # JavaScript
```

---

## 🔧 Key Features

✅ **Employee Module**
- Register & Login
- Apply for leave (Casual, Sick, Earned)
- View leave history
- Track leave balance
- Manage profile

✅ **Admin Module**
- Review leave requests
- Approve/Reject leave
- Manage employees
- View employee details
- Analytics dashboard

✅ **Security**
- Password hashing (Werkzeug)
- Session management
- Login required decorators
- Input validation

---

## 📊 Database Models

**Employees Table:**
- emp_id, name, email, password
- department, designation, phone, join_date
- casual_balance, sick_balance, earned_balance

**Leave Requests Table:**
- employee_id, leave_type, start_date, end_date
- total_days, reason, status, admin_remarks

**Admins Table:**
- name, email, password

---

## 🚀 Troubleshooting

**Issue: Port 5000 already in use**
```python
# Edit the last line of app.py:
app.run(debug=True, port=5001)
```

**Issue: Database already exists**
```bash
# Delete the old database and start fresh:
del leave_management.db
```

Then re-run: `/init_db` and `/seed_admin`

---

## 📝 Notes

- All dates are in `YYYY-MM-DD` format
- Leave balance defaults: Casual (12), Sick (10), Earned (15)
- Overlapping leave requests are prevented
- Admin approval deducts leave balance automatically

Enjoy! 🎉
