# Demo Blog Site Using Django

## About

This is a demo project for practicing Django.
The idea was to build some basic blogging platform.

It was made using **Python 3.6** + **Django 3.2** and database is **SQLite3**.


User has his own blog page, where he can add new blog posts. 
Home page is paginated list of all posts.
Non-authenticated users can see all blog posts, but cannot add new posts or comment.


## Prerequisites

\[Optional\] Install virtual environment:

```bash
$ python -m virtualenv env
```

\[Optional\] Activate virtual environment:

On macOS and Linux:
```bash
$ source env/bin/activate
```

On Windows:
```bash
$ .\env\Scripts\activate
```

Install dependencies:
```bash
$ pip install -r requirements.txt
```

## Installing	Django with pip

Run	the	following command	at the shell prompt to install Django with pip:


```bash
pip install Django==2.0.5
```
Check	whether	Django has been successfully installed.

```bash
>>> import django
>>> django.get_version()
    '2.0.5'
```

## Post Installation

Go to the web browser and visit `http://127.0.0.1:8000/`

Admin username: **admin**

Admin password: **adminpassword**

## Creating project

Create an initial project file structure.

```bash
$ django-admin startproject mysite
```
This will create a Django project with the name mysite which includes files namely:
- manage.py
- __init__.py
- settings.py
- urls.py
- wsgi.py

To complete the project setup, we will need	to create the tables in the	database required by the applications listed in INSTALLED_APPS. Open the shell and run the following commands:

```bash
cd mysite
python manage.py migrate
```
### Running the	development server
You can run the application from the command line with manage.py.
Go to the root folder of the application.

Run server:
```bash
$ python manage.py runserver 
```

### Create the application blog within mysite project

From the project's root	directory, Run the following command:
```bash
$ python manage.py startapp	blog
```

This will create the basic structure of the application, which includes files namely:
__init__.py
admin.py
apps.py
migrations/
	__init__.py
models.py
tests.py
views.py



## Helper Tools

### Django Admin

It is possible to add additional admin user who can login to the admin site. Run the following command:
```bash
$ python manage.py createsuperuser
```
Enter your desired username and press enter.
```bash
Username: admin_username
```

You will then be prompted for your desired email address:
```bash
Email address: admin@example.com
```

The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first.
```bash
Password: **********
Password (again): *********
Superuser created successfully.
```

Go to the web browser and visit `http://127.0.0.1:8000/admin`



