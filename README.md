# 🏥 Hospital Management System

A role-based Hospital Management System (HMS) web application built using **Flask**, **MySQL**, and **Flask extensions**. This system allows multiple types of users (Admin, Doctor, Front Desk, Data Entry) to interact with hospital data securely and efficiently.

---

## 🚀 Features

### ✅ User Roles
- **Admin:** Manage users, doctors, rooms, and reset passwords.
- **Doctor:** View appointments, enter treatments, prescribe medications, and order tests.
- **Front Desk:** Book appointments, check doctor availability.
- **Data Entry:** Register/edit patient data, assign rooms, manage patient status.

### 📋 Modules
- **Authentication & Authorization** using `Flask-Login`
- **Secure Passwords** with `Flask-Bcrypt`
- **Form Validation** via `Flask-WTF` and `WTForms`
- **Email OTP for password reset** using `Flask-Mail`
- **Role-specific Dashboards**
- **Room allocation and occupancy tracking**
- **Appointments & time slot management**
- **Treatment, Prescription, Test records**

---

## 🛠 Tech Stack

| Layer        | Technology |
|--------------|------------|
| Backend      | Flask (Python) |
| Database     | MySQL |
| Frontend     | HTML, CSS (role-based styles) |
| Auth         | Flask-Login, Flask-Bcrypt |
| Forms        | Flask-WTF, WTForms |
| Email        | Flask-Mail |
| Validation   | validate-email-address |
| ORM/SQL      | mysql-connector-python |

---

## 📁 Project Structure

```

hospital-management-system/
│
├── app.py               # Flask app routes
├── db.py                # Database helper functions
├── requirements.txt     # Python dependencies
│
├── static/
│   └── css/
│       ├── admin.css
│       ├── common.css
│       ├── data.css
│       ├── doctor.css
│       ├── front.css
│       └── login.css
│
├── templates/
│   ├── login.html
│   ├── admin/
│   ├── doctor/
│   ├── front\_desk/
│   └── data\_entry/
│
└── README.md            # This file

````

---

## 🔧 Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/hospital-management-system.git
cd hospital-management-system
````

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Set up MySQL database

* Create a database (e.g., `hospital_db`)
* Import your schema (users, doctors, rooms, appointments, etc.)
* Update `db.py`:

```python
password="yourpassword"
database="hospital_db"
```

### 4. Run the Flask app

```bash
python app.py
```

---

## 📧 Email OTP Setup (Optional)

To enable password reset via email:

* Set up a Gmail or SMTP account
* Configure `Flask-Mail` in your app:

```python
app.config['MAIL_SERVER'] = 'smtp.gmail.com'
app.config['MAIL_PORT'] = 587
app.config['MAIL_USERNAME'] = 'your_email@gmail.com'
app.config['MAIL_PASSWORD'] = 'your_app_password'
```

---

## 📌 Future Improvements

* Add pagination and search in lists
* Role-based menu hiding via Jinja2
* API endpoints for external integration
* Docker support

---

## 👨‍💻 Developed By

* **Navya Varri**
