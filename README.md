# AcademicGuard

## Behavioral Fraud Detection for Digital Academic Certification Systems

AcademicGuard is a Django-based proof-of-concept web application designed to detect suspicious user behavior associated with digital academic certificates.

The project focuses on using behavioral activity data and machine learning concepts to identify potentially fraudulent or suspicious certificate access patterns.

## Features

* Secure user login
* Academic fraud detection
* User activity monitoring
* Certificate verification
* Fraud detection results
* Risk-level classification
* Security score
* Detection reports
* Django administration panel
* Database management using SQLite
* Responsive web interface

## Technology Stack

### Backend

* Python
* Django

### Database

* SQLite

### Machine Learning

* Logistic Regression
* SMOTE for handling class imbalance
* Behavioral feature analysis

### Frontend

* HTML
* CSS
* JavaScript

### Development Tools

* Git
* GitHub
* Visual Studio Code

## Project Structure

```text
academic_fraud_detection/
│
├── manage.py
├── db.sqlite3
│
├── fraud_detection/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
└── academic/
    ├── admin.py
    ├── apps.py
    ├── models.py
    ├── urls.py
    ├── views.py
    │
    ├── templates/
    │   └── academic/
    │       ├── home.html
    │       ├── login.html
    │       ├── dashboard.html
    │       ├── detection.html
    │       ├── certificate_verification.html
    │       ├── reports.html
    │       └── result.html
    │
    └── static/
        └── academic/
            ├── style.css
            └── js/
                └── home.js
```

## Main Modules

### User Activity Monitoring

Records information such as:

* IP address
* Location
* Device
* Access time
* Certificate ID
* Access frequency
* Status
* Risk level
* Security score

### Certificate Verification

The system allows a certificate ID to be checked against the certificate database.

Certificate statuses include:

* Verified
* Pending
* Invalid

### Fraud Detection

The application analyzes user activity and produces a detection result containing:

* Prediction
* Probability
* Risk level
* Security score
* Model name

## Machine Learning Approach

The proposed machine learning approach uses **Logistic Regression** for behavioral fraud detection.

The planned workflow is:

```text
Dataset
   ↓
Data Preprocessing
   ↓
Feature Selection
   ↓
SMOTE
   ↓
Train/Test Split
   ↓
Logistic Regression
   ↓
Model Evaluation
   ↓
Save Trained Model
   ↓
Integrate Model with Django
   ↓
Fraud Prediction
```

## Current Project Status

The Django web application currently provides the main user interface, database models, administration features, certificate verification, user activity recording, and fraud detection result management.

The current detection logic is a proof-of-concept demonstration. The trained Logistic Regression model will be integrated into the Django application as the machine-learning component.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/academic-fraud-detection.git
```

Move into the project directory:

```bash
cd academic-fraud-detection
```

Install the required dependencies:

```bash
pip install django
```

Run database migrations:

```bash
python manage.py migrate
```

Create an administrator account:

```bash
python manage.py createsuperuser
```

Start the development server:

```bash
python manage.py runserver
```

Open:

```text
http://127.0.0.1:8000/
```

## Admin Panel

The Django administration panel is available at:

```text
http://127.0.0.1:8000/admin/
```

The admin panel can be used to manage:

* User Activities
* Certificates
* Fraud Detection Results

## Future Enhancements

* Integrate the trained Logistic Regression model
* Add real-time fraud prediction
* Add data visualization dashboards
* Add authentication and role-based access
* Add advanced behavioral features
* Add model performance metrics
* Add fraud trend analysis
* Deploy the application to a cloud platform

## Disclaimer

This project is developed as a proof-of-concept academic project for studying behavioral fraud detection in digital academic certification systems.
