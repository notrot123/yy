# [Django](https://appseed.us/apps/django/) Boilerplate 

Reference codebase used by AppSeed in all [Django Apps](https://appseed.us/apps/django/) starters.

<br /> 

> 🚀 Built with [App Generator](https://appseed.us/generator/), Timestamp: `2022-06-06 13:47`

- `Up-to-date dependencies`
- Database: `sqlite`
- UI-Ready app, Django Native ORM
- `Session-Based authentication`, Forms validation
- 👉 [Complete documentation](https://docs.appseed.us/boilerplate-code/django) - `Learn how to use and update the product`
  - ✅ [Set up the environment](https://docs.appseed.us/boilerplate-code/django#environment)
  - ✅ [Manage App users](https://docs.appseed.us/boilerplate-code/django#manage-app-users)
  - ✅ [Application Bootstrap Flow](https://docs.appseed.us/boilerplate-code/django#application-bootstrap-flow)
  - ✅ [App Routing](https://docs.appseed.us/boilerplate-code/django#project-routing)
  - ✅ [UI Assets and Templates](https://docs.appseed.us/boilerplate-code/django#ui-assets-and-templates)
  - ✅ [Set up the MySql Database](https://docs.appseed.us/boilerplate-code/django#set-up-the-mysql-database)
  - ✅ [Adding a new app](https://docs.appseed.us/boilerplate-code/django#adding-a-new-app)
  - ✅ [Static Assets for production](https://docs.appseed.us/boilerplate-code/django#static-assets-for-production)  

<br />

![Material Kit - Starter generated by AppSeed.](https://user-images.githubusercontent.com/51070104/167396765-c88b7a95-155f-4236-8691-7b80fa2d9cd9.png)

<br />


## ✨ Start the app in Docker

> 👉 **Step 1** - Download the code from the GH repository (using `GIT`) 

```bash
$ git clone https://github.com/app-generator/boilerplate-code-django.git
$ cd boilerplate-code-django
```

<br />

> 👉 **Step 2** - Start the APP in `Docker`

```bash
$ docker-compose up --build 
```

Visit `http://localhost:5085` in your browser. The app should be up & running.

<br />

## ✨ How to use it

> Download the code 

```bash
$ git clone https://github.com/app-generator/boilerplate-code-django.git
$ cd boilerplate-code-django
```

<br />

### 👉 Set Up for `Unix`, `MacOS` 

> Install modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

### 👉 Set Up for `Windows` 

> Install modules via `VENV` (windows) 

```
$ virtualenv env
$ .\env\Scripts\activate
$ pip3 install -r requirements.txt
```

<br />

> Set Up Database

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

> Start the app

```bash
$ python manage.py runserver
```

At this point, the app runs at `http://127.0.0.1:8000/`. 

<br />

## ✨ Create Users

By default, the app redirects guest users to authenticate. In order to access the private pages, follow this set up: 

- Start the app via `flask run`
- Access the `registration` page and create a new user:
  - `http://127.0.0.1:8000/register/`
- Access the `sign in` page and authenticate
  - `http://127.0.0.1:8000/login/`

<br />

## ✨ Code-base structure

The project is coded using a simple and intuitive structure presented below:

```bash
< PROJECT ROOT >
   |
   |-- core/                               # Implements app configuration
   |    |-- settings.py                    # Defines Global Settings
   |    |-- wsgi.py                        # Start the app in production
   |    |-- urls.py                        # Define URLs served by all apps/nodes
   |
   |-- apps/
   |    |
   |    |-- home/                          # A simple app that serve HTML files
   |    |    |-- views.py                  # Serve HTML pages for authenticated users
   |    |    |-- urls.py                   # Define some super simple routes  
   |    |
   |    |-- authentication/                # Handles auth routes (login and register)
   |    |    |-- urls.py                   # Define authentication routes  
   |    |    |-- views.py                  # Handles login and registration  
   |    |    |-- forms.py                  # Define auth forms (login and register) 
   |    |
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/                     # Templates used to render pages
   |         |-- includes/                 # HTML chunks and components
   |         |    |-- navigation.html      # Top menu component
   |         |    |-- footer.html          # App Footer
   |         |    |-- scripts.html         # Scripts common to all pages
   |         |
   |         |-- layouts/                   # Master pages
   |         |    |-- base.html             # Used by common pages
   |         |
   |         |-- accounts/                  # Authentication pages
   |         |    |-- login.html            # Login page
   |         |    |-- register.html         # Register page
   |         |
   |         |-- home/                      # UI Kit Pages
   |              |-- index.html            # Index page
   |              |-- page-404.html         # 404 page
   |              |-- *.html                # All other pages
   |
   |-- requirements.txt                     # Development modules - SQLite storage
   |
   |-- .env                                 # Inject Configuration via Environment
   |-- manage.py                            # Start the app - Django default start script
   |
   |-- ************************************************************************
```

<br />

---
[Django](https://appseed.us/apps/django/) Boilerplate  - Open-source starter generated by **[App Generator](https://appseed.us/generator/)**.
