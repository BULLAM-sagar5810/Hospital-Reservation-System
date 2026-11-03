# 🏥 Hospital Reservation System

A full-stack web application designed to simplify hospital appointment management and improve communication between patients, doctors, and hospital administrators.

The Hospital Reservation System provides a centralized platform where patients can access hospital services, manage their accounts, and interact with appointment-related functionality through a user-friendly interface.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Project Objectives](#-project-objectives)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [System Architecture](#-system-architecture)
- [Project Structure](#-project-structure)
- [Prerequisites](#-prerequisites)
- [Installation and Setup](#-installation-and-setup)
- [Running the Application](#-running-the-application)
- [API Documentation](#-api-documentation)
- [Testing the Application](#-testing-the-application)
- [Application Workflow](#-application-workflow)
- [Security Considerations](#-security-considerations)
- [Future Enhancements](#-future-enhancements)
- [Learning Outcomes](#-learning-outcomes)
- [Author](#-author)

---

## 📖 Project Overview

The Hospital Reservation System is a full-stack web application developed to make hospital appointment-related operations easier and more efficient.

Traditional hospital appointment processes can involve long waiting times, manual paperwork, and difficulty managing patient information.

This application aims to simplify these processes by providing a digital platform for hospital-related services.

Patients can interact with the application through the frontend, while the backend processes requests and communicates with the database.

The application follows a frontend-backend architecture using React.js and Django.

---

## 🎯 Project Objectives

The main objectives of this project are:

- Develop a user-friendly hospital management interface.
- Simplify patient registration and authentication.
- Provide a centralized platform for patient-related information.
- Support appointment-related operations.
- Build REST API-based communication between frontend and backend.
- Store and manage application data using a database.
- Understand real-world full-stack application development.

---

## 🚀 Key Features

### 1. User Authentication
- User registration.
- User login.
- Authentication-related API endpoints.
- Secure handling of user credentials through the backend.

### 2. Patient Management
- Patient-related information management.
- Patient API endpoints.
- Centralized patient data handling.

### 3. Hospital Dashboard
- Dashboard-related functionality.
- Access to relevant application information.
- Organized presentation of available data.

### 4. Appointment Management
- Appointment-related functionality.
- Support for hospital appointment workflows.
- Integration with backend APIs.

### 5. API Documentation
- API schema generation.
- Interactive API documentation.
- Ability to inspect and test available endpoints.

*Note: The availability of individual features depends on the actual implementation in the source code.*

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Webpage structure |
| CSS3 | Styling and responsive layouts |
| JavaScript | Frontend functionality |
| React.js | Frontend user interface |
| Python | Backend programming |
| Django | Backend framework |
| REST APIs | Frontend-backend communication |
| SQL Database | Data storage |
| Git | Version control |
| GitHub | Source code management |
| VS Code | Development environment |

---

## 🏗️ System Architecture

The application follows a client-server architecture.

```text
             PATIENT / ADMIN
                    |
                    |
                    v
          +-------------------+
          |    React.js       |
          |    Frontend       |
          +-------------------+
                    |
                    |
               HTTP Requests
                    |
                    v
          +-------------------+
          |    Django         |
          |    Backend        |
          +-------------------+
                    |
                    |
               REST APIs
                    |
                    v
          +-------------------+
          |   SQL Database    |
          |   Data Storage    |
          +-------------------+
```

### How It Works

1. The user opens the hospital application.
2. React.js displays the user interface.
3. The user performs an action, such as logging in or accessing patient information.
4. React.js sends an HTTP request to the Django backend.
5. Django processes the request.
6. The backend communicates with the configured database when required.
7. Django returns a response to the frontend.
8. React.js displays the result to the user.

---

## 📂 Project Structure

The following is an illustrative project structure. Your actual folders and filenames may differ.

```text
hospital-reservation-system/
│
├── backend/
│   │
│   ├── manage.py
│   ├── requirements.txt
│   │
│   ├── config/
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── ...
│   │
│   ├── accounts/
│   ├── patients/
│   ├── doctors/
│   ├── appointments/
│   │
│   └── ...
│
├── frontend/
│   │
│   ├── package.json
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   └── ...
│   │
│   └── ...
│
└── README.md
```

---

## 💻 Prerequisites

Install the following software before running the project:

| Software | Purpose |
|---|---|
| Python 3 | Backend development |
| Node.js and npm | Frontend development |
| VS Code | Code editor |
| Git | Version control |
| Web Browser | Application testing |

Check the installations:

```bash
python --version
```

```bash
node --version
```

```bash
npm --version
```

If PowerShell blocks the npm PowerShell script, use:

```powershell
npm.cmd --version
```

---

## ⚙️ Installation and Setup

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

Navigate into the project:

```bash
cd hospital-reservation-system
```

### Step 2: Backend Setup

Navigate to the backend directory:

```bash
cd backend
```

Create a Python virtual environment:

```bash
python -m venv venv
```

Activate the virtual environment in Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, you can use:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then activate again.

### Step 3: Install Backend Dependencies

Upgrade pip:

```bash
python -m pip install --upgrade pip
```

Install the required packages:

```bash
python -m pip install -r requirements.txt
```

### Step 4: Database Migration

Run:

```bash
python manage.py makemigrations
```

Then:

```bash
python manage.py migrate
```

These commands prepare the database according to the Django models and migrations.

### Step 5: Create an Admin User

```bash
python manage.py createsuperuser
```

Follow the instructions to create the administrator account.

---

## ▶️ Running the Application

The backend and frontend should run in separate terminals.

### Terminal 1: Start Django Backend

Open the backend directory and activate the virtual environment.

Run:

```bash
python manage.py runserver
```

Backend URL:

```text
http://127.0.0.1:8000/
```

### Terminal 2: Start React Frontend

Open another VS Code terminal.

Navigate to the frontend directory:

```bash
cd frontend
```

Install frontend dependencies:

```powershell
npm.cmd install
```

Start the frontend:

```powershell
npm.cmd run dev
```

Open the local frontend address displayed in the terminal. For a standard Vite setup, it is usually:

```text
http://localhost:5173/
```

**Important:** The frontend port and available npm scripts depend on the actual `package.json` configuration.

---

## 🔗 API Documentation

The Django backend provides API-related URL routes.

Based on the current project URL configuration, the following routes are available:

| Endpoint | Purpose |
|---|---|
| `/api/auth/` | Authentication-related APIs |
| `/api/patients/` | Patient-related APIs |
| `/api/` | Additional application API routes |
| `/api/dashboard/` | Dashboard-related APIs |
| `/api/schema/` | API schema |
| `/api/docs/` | Interactive API documentation |
| `/admin/` | Django administration |

### Open API Documentation

```text
http://127.0.0.1:8000/api/docs/
```

Use the documentation to inspect the available endpoints, request methods, parameters, and responses.

---

## 🧪 Testing the Application

Testing helps verify whether the application works correctly.

### 1. Frontend Testing

- Open the frontend application.
- Check whether the home page loads.
- Verify the navigation links.
- Check the form fields and buttons.
- Verify the page layout.

### 2. Backend Testing

Open:

```text
http://127.0.0.1:8000/api/docs/
```

Inspect the available API endpoints and test supported requests.

### 3. Authentication Testing

If registration and login are implemented, test:

- Valid user registration.
- Invalid registration details.
- Valid login credentials.
- Invalid login credentials.
- Required-field validation.

### 4. Patient API Testing

If patient operations are implemented, test:

- Retrieving patient information.
- Creating patient records.
- Updating patient information.
- Handling invalid requests.

### 5. Django Unit Tests

Run:

```bash
python manage.py test
```

This executes the Django tests available in the project.

---

## 🔄 Application Workflow

The general workflow of the Hospital Reservation System is:

```text
        Start Application
               |
               v
        Open Website
               |
               v
        User Registration
               |
               v
           User Login
               |
               v
       Access Application
               |
               v
       Patient Operations
               |
               v
      Appointment Workflow
               |
               v
        Backend Processing
               |
               v
        Database Operations
               |
               v
        Response to Frontend
               |
               v
          End Process
```

---

## 🔐 Security Considerations

Security is important when developing applications that handle patient information.

Recommended security practices include:

- Use Django's authentication system.
- Store passwords using secure password hashing.
- Validate user input on the backend.
- Use appropriate authentication and authorization.
- Keep secret keys outside public source code.
- Configure environment variables for sensitive settings.
- Use HTTPS when deploying the application.
- Avoid uploading real patient information to public repositories.

**Important:** Use sample data for development and testing. Do not use real patient medical information in a public demo.

---

## 🔮 Future Enhancements

The following features can be considered for future development:

1. Online appointment confirmation.
2. Doctor availability management.
3. Email and SMS appointment notifications.
4. Appointment cancellation and rescheduling.
5. Online payment integration.
6. Patient medical history management.
7. Prescription management.
8. Hospital analytics dashboard.
9. Role-based access control.
10. Cloud deployment.

---

## 📚 Learning Outcomes

By developing this project, I gained practical exposure to:

- Frontend development using React.js.
- Backend development using Python and Django.
- REST API concepts and integration.
- Database management.
- Full-stack application architecture.
- Request and response handling.
- Debugging and application testing.
- Git and GitHub project management.

---

## 👨‍💻 Author

**Bullam Sagar**

Computer Science and Engineering | Big Data Analytics

**GitHub:**  
https://github.com/BULLAM-sagar5810

**LinkedIn:**  
https://www.linkedin.com/in/bullam-sagar-42281a273

**Portfolio:**  
https://sagar-portfolio-kappa-opal.vercel.app/

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

Thank you for visiting the Hospital Reservation System project!
