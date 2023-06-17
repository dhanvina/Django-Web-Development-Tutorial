# Django-Web-Development-Tutorial
In this comprehensive Django tutorial, you will learn how to build dynamic web application using powerful Python web framework, Django.

1. Introduction to Django:
  * Understanding the basics of Django, it's architecture and advantages of using it.
  * Setup a development environment for Django projects
  * Create a Django project and familiarize with files created by Django.
  
2. Django Models and Databases:
  * Learn how to define models for ER diagrams.
  * Understanding Django's ORM features and it's interaction with database.
  
3. Django Views and templates:
  * Explore the concepts of Views and learn how to handle user requests.
  * Create templates to generate dynamic HTML pages and manipulate data within the pages.
  
4. URL routing:
  * Understand URL roouting in Django and how to map URL's to views.
  
5. Django Forms and User inputs:
  * Learn User authentication functionality with it's in-built user model.
  * Validate and process forms in views.
  * Customize form rendering. 
  
6. Django's Authentication:
  * Explore different authentication methods and implement user roles and permissions.

7. Django's Admin Interface:
  * Understanding Django's powerful admin functionalities.
 
## Using a virtual environment in Django is important because it:

1. Ensures dependency isolation, preventing conflicts with other projects or the system's Python installation.
2. Provides reproducibility by specifying the exact versions of packages used in the project.
3. Enables portability, allowing easy sharing and deployment across different machines or servers.
4. Simplifies package management, with a dedicated space for installing, updating, and removing packages.
5. Facilitates testing and development by providing an isolated environment to experiment without affecting the system. 

# How to setup Django project ?
1. <b>pipenv install Django</b> - When you run "pipenv install Django," the following actions take place:
 * Pipenv checks if a Pipfile exists in your project directory. The Pipfile is a configuration file that specifies the project's dependencies.
 * If a Pipfile is not found, Pipenv creates a new one.
 * Pipenv analyzes the specified dependencies in the Pipfile and resolves the versions required for each package, including Django and its dependencies.
 * Pipenv creates a virtual environment specifically for your project, isolating its dependencies from the system-wide Python installation and other projects.
 * Pipenv installs Django and its dependencies into the virtual environment, ensuring that the required versions are available for your project.
2. <b>pipenv shell</b> - When you run "pipenv shell" the following actions take place:
 * Pipenv checks if a virtual environment exists for your project. If it doesn't, it creates a new virtual environment.
 * If the virtual environment exists or is created, Pipenv activates it, making it the active environment for your current terminal session.
 * Once the virtual environment is activated, the command prompt in your terminal will change to indicate that you are now working within the virtual environment.
 * Any subsequent Python or pip commands you run within the same terminal session will use the packages installed in the virtual environment rather than the system-wide Python installation.
3. <b>django-admin startproject projectname</b> - When you run this command, the following actions take place:
 * Django's administrative script, "django-admin," is executed to initiate the project creation process.
 * A new directory with the specified "filename" is created in the current directory. This directory will serve as the root directory of your Django project.
 * Several files and directories are generated within the project directory, including:
     * The project's main configuration file, "settings.py," which contains settings and configuration options for the Django project.
     * A "urls.py" file, which defines the URL routing patterns for the project.
     * An empty "wsgi.py" file, which is used for serving the Django project via the WSGI protocol.
     * A "manage.py" script, which provides a command-line interface for managing various aspects of the Django project.
 * The project directory is set up with a basic structure and configuration, allowing you to start developing your Django application within it.
 
- projectname/
  - projectname/
    - __init__.py
    - asgi.py
    - settings.py
    - urls.py
    - wsgi.py
  - manage.py




In Django, a <b>project</b> and an <b>app</b> are two distinct concepts:

### Django Project:
 * A Django project is a collection of settings, configurations, and applications that together form a complete web application.
 * It serves as the container for your entire web application and encompasses the settings, URL configurations, database settings, and other project-level configurations.
 * A Django project can contain multiple apps.
 * When you create a Django project using the <b>django-admin startproject</b>. command, it generates the project's root directory along with essential files such as settings.py, urls.py, and manage.py.

### Django App:
 * A Django app is a modular component that encapsulates a specific functionality or feature of a web application.
 * It represents a self-contained module within a Django project that provides a specific set of functionalities.
 * Apps are typically designed to be reusable and can be plugged into different projects.
 * An app can include models, views, templates, static files, and URL routing specific to its functionality.
 * It can also contain other resources like forms, helpers, middleware, and management commands.
 * You can create a Django app within a project using the <b>python manage.py startapp</b> command.
 * This command generates a directory for the app with a predefined structure and files such as models.py, views.py, and urls.py. You can then customize and extend the app according to your application's requirements.
 
4. <b>python manage.py startapp app_name</b> - By using the command python manage.py startapp <app_name>, where <app_name> is the name you provide for your app, you will generate a new Django app within your project. This command performs the following actions:

 * Creates a new directory for your app: The command creates a new directory with the specified <app_name>, this directory will contain all the files and modules specific to your app.

 * Generates necessary files and directories: Inside the app directory, the command generates several files and directories with a predefined structure:

   * __init__.py: This empty file indicates that the app directory is a Python package and allows other modules to be imported from within this directory.
   * admin.py: This file is used for registering models with the Django admin interface. You can define how your app's models should be displayed and managed in the admin interface.
   * apps.py: This file contains the app configuration, including the name and any additional settings specific to the app.
   * models.py: This file is where you define your app's data models using Django's Object-Relational Mapping (ORM). You can define database tables, fields, relationships, and behavior of your app's data objects.
   * tests.py: This file is meant for writing test cases for your app. You can define unit tests, integration tests, and other tests to ensure the functionality of your app.
   * views.py: This file is used for defining the views or endpoints of your app. Views handle incoming requests, process data, and return responses.

 * Registers the app in the project's settings: When you create a new app using startapp, it automatically adds the app to the project's list of installed apps in the settings.py file. This ensures that your app is recognized and integrated into the Django project.


- project-name/
  - app-name/
    - migrations/
      - __init__.py
    - __init__.py
    - admin.py
    - apps.py
    - models.py
    - tests.py
    - views.py
  - project-name/
    - __init__.py
    - asgi.py
    - settings.py
    - urls.py
    - wsgi.py
  - manage.py
