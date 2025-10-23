Medical Portal

A simple Django-based web application that allows Patients and Doctors to sign up, log in, and view their dashboards.

The application includes:

User Types: Patient and Doctor

Signup Form: Captures user details and profile picture

Login: Redirects users to their respective dashboards

Dashboards: Display user information with profile picture, address, and email

Profile Picture Handling: Shows a placeholder if no picture is uploaded

Features

User Types

Patient

Doctor

Signup Form Fields

First Name

Last Name

Profile Picture

Username

Email

Password and Confirm Password

Address (Line 1, City, State, Pincode)

Validation

Password and Confirm Password must match

Email and username uniqueness validation

Dashboard

Displays user's details and profile picture

Placeholder avatar if picture is missing

Logout functionality

UI

Modern and interactive interface using HTML, CSS, and JS

Responsive design for mobile devices

Installation

Clone the repository

git clone <repository_url>
cd medical_portal


Create a virtual environment

python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate


Install dependencies

pip install -r requirements.txt


Apply migrations

python manage.py migrate


Create superuser (optional)

python manage.py createsuperuser


Run the server

python manage.py runserver


Access the application
Open your browser and go to http://127.0.0.1:8000/signup/ to create a user.

Project Structure
medical_portal/
│
├── accounts/                # Django app for user accounts
│   ├── templates/accounts/  # HTML templates for signup, login, dashboards
│   ├── static/accounts/     # CSS and JS files
│   ├── models.py            # Custom User model with profile_picture and address
│   ├── forms.py             # Signup and login forms
│   └── views.py             # Signup, login, logout, and dashboard views
│
├── medical_portal/          # Project settings
├── db.sqlite3               # Database file
├── manage.py                # Django management script
└── requirements.txt         # Project dependencies

Dependencies

Python 3.12+

Django 5.1+

Pillow (for handling profile pictures)




Notes

Profile pictures are stored in MEDIA_ROOT. Make sure MEDIA_URL and MEDIA_ROOT are configured in settings.py.

This is a basic implementation. No advanced authentication or role-based permissions beyond patient/doctor differentiation.
