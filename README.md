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
 Example's for these files:
 * manage.py-
 
