

# Medical Portal

A simple **Django-based web application** that allows **Patients** and **Doctors** to sign up, log in, and view their dashboards.

The application includes:

* **User Types:** Patient and Doctor
* **Signup Form:** Captures user details and profile picture
* **Login:** Redirects users to their respective dashboards
* **Dashboards:** Display user information with profile picture, address, and email
* **Profile Picture Handling:** Shows a placeholder if no picture is uploaded

---

## Features

1. **User Types**

   * Patient
   * Doctor

2. **Signup Form Fields**

   * First Name
   * Last Name
   * Profile Picture
   * Username
   * Email
   * Password and Confirm Password
   * Address (Line 1, City, State, Pincode)

3. **Validation**

   * Password and Confirm Password must match
   * Email and username uniqueness validation

4. **Dashboard**

   * Displays user's details and profile picture
   * Placeholder avatar if picture is missing
   * Logout functionality

5. **UI**

   * Modern and interactive interface using HTML, CSS, and JS
   * Responsive design for mobile devices

---

## Installation

1. **Clone the repository**

```bash
git clone <repository_url>
cd medical_portal
```

2. **Create a virtual environment**

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Apply migrations**

```bash
python manage.py migrate
```

5. **Create superuser (optional)**

```bash
python manage.py createsuperuser
```

6. **Run the server**

```bash
python manage.py runserver
```

7. **Access the application**
   Open your browser and go to `http://127.0.0.1:8000/signup/` to create a user.

---

## Project Structure

```
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
```

---

## Dependencies

* Python 3.12+
* Django 5.1+
* Pillow (for handling profile pictures)

---



## Notes

* Profile pictures are stored in `MEDIA_ROOT`. Make sure `MEDIA_URL` and `MEDIA_ROOT` are configured in `settings.py`.
* This is a **basic implementation**. No advanced authentication or role-based permissions beyond patient/doctor differentiation.

---

