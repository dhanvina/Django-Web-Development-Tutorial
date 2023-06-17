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

5. <b>python manage.py runserver</b>: The command python manage.py runserver is used to start the development server provided by Django. When you run this command, it performs the following actions:
 * Checks the project's configuration: The command checks the project's configuration files, such as settings.py, to ensure that all necessary settings are properly defined. This includes database settings, installed apps, middleware, static file configurations, and more.
 * Sets up the development server: The command sets up a lightweight development server, which listens for incoming HTTP requests on a specified host and port. By default, the server listens on 127.0.0.1 (localhost) and port <b>8000</b>.
 * Loads the Django project: The command loads your Django project, including the project-level settings, URL configurations, and other necessary components.
 * Starts the development server: Once everything is set up, the command starts the development server, which is responsible for handling incoming HTTP requests and dispatching them to the appropriate Django views and URL patterns.
 * Displays server information: After the server is successfully started, it displays information about the server, such as the host and port where it's running. It also provides information about the Django version and other relevant details.

![Screenshot (93)_WPS Photo](https://github.com/dhanvina/Django-Web-Development-Tutorial/assets/47035051/4ca90df4-0106-4bb6-875b-4d42450ca9df)

## Let's create a small html file to display on your browser

1. <b>python manage.py startapp testapp</b> - Again, it creates all the required files for the application.
2. Go to projects/settings.py - 
```
INSTALLED_APPS = [
     'django.contrib.admin',
     'django.contrib.auth',
     'django.contrib.contenttypes',
     'django.contrib.sessions',
     'django.contrib.messages',
     'django.contrib.staticfiles',
     'testapp', #add the appname 
 ]
```
 * Adding the line 'testapp' to the INSTALLED_APPS list in settings.py is necessary to inform your Django project that the "hello_world" app exists and should be included in the project's functionality. This step is required for Django to recognize and load the app's components correctly.
                       
3. we have to create a view:
 * In Django, a view is a Python function or method that receives an HTTP request and returns an HTTP response.
 *  It is responsible for handling the logic associated with a specific URL pattern and generating the appropriate response for that request.
 * Views act as the intermediary between the user's request and the corresponding actions or data manipulations that need to be performed.
 *  They define what happens when a particular URL is accessed by the user.
 *  In Django, views can be defined in various ways:
   * Function-based views: Views can be written as Python functions that take a request as the first parameter and return an HttpResponse or a subclass of HttpResponse.
   * Class-based views: Views can be written as classes that inherit from Django's View or other specialized view classes. These classes provide methods that handle different HTTP methods (such as GET, POST, etc.) and encapsulate common functionality.
   * Generic views: Django provides a set of pre-built generic views that simplify the creation of common views, such as list views, detail views, form views, and more. These views are often used for CRUD operations (Create, Retrieve, Update, Delete).
   * Views can perform various tasks, including:
     * Fetching data from a database or other data source.
     * Processing user input or form submissions.
     * Rendering HTML templates with dynamic data.
     * Handling redirects or rendering JSON responses.
     * Accessing session data or authentication information.
     * Performing data manipulations or calculations.
 * Navigate to views.py in testapp directory and add the code:
 * ```
    from django.shortcuts import render
    def hello_world(request):
         return render(request, 'hello_world.html', {})
   ```
 ```render(request, template_name, context=None, content_type=None, status=None, using=None)```
   * request: The first parameter, request, represents the incoming HTTP request made by a user. It is required and specifies the request object.
   * template_name: The second parameter, template_name, is a string that specifies the name of the template to be rendered. This can be a path to the template file or a template name registered with Django's template loader.
   * context=None: The third parameter, context, is an optional parameter that specifies a dictionary containing the context variables to be passed to the template. Context variables provide data to be used within the template, such as dynamic content or data fetched from a database. If not provided, an empty dictionary {} is used as the default value.
   * content_type=None: The content_type parameter is an optional parameter that specifies the content type of the response. It determines how the response is interpreted by the browser. If not provided, Django uses the default content type, which is 'text/html' for HTML responses.
   * status=None: The status parameter is an optional parameter that specifies the HTTP status code for the response. If not provided, Django uses 200 (OK) as the default status code.
   * using=None: The using parameter is an optional parameter used when working with multiple template engines. It specifies the name of the template engine to be used for rendering the template. If not provided, Django uses the default template engine specified in the project's settings.
 * Example 1: Rendering a template without context variables 

```
from django.shortcuts import render

def hello(request):
    return render(request, 'hello.html')
```
In this example, the home() view function renders the template 'home.html' without passing any context variables. The rendered template will be returned as an HTTP response.
 * Example 2: Rendering a template with context variables

```
from django.shortcuts import render

def product_details(request, product_id):
    product = get_product_by_id(product_id)
    context = {'product': product}
    return render(request, 'product_details.html', context)
```
In this example, the product_details() view function renders the template 'product_details.html' and passes a context variable named 'product' containing the details of a product. The context variable is accessed within the template to display dynamic content related to the specific product.
 * Example 3: Rendering a template with a custom status code
```
from django.shortcuts import render

def unauthorized(request):
    return render(request, 'unauthorized.html', status=401)
    
```
In this example, the unauthorized() view function renders the template 'unauthorized.html' and returns it as an HTTP response with a status code of 401 (Unauthorized). This can be used to indicate to the user that they are not authorized to access the requested resource.

4. Create a templates folder under testapp directory which contains all the templates to be displayed. Example: html files.
```
mkdir testapp/templates/hello.html
```
```
<h1>Hello User!!</h1>
```
Now we have created functions to handle users views and templates.
5. Hookup URL's - 
```
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('hello.urls')),
]
```
  * from django.contrib import admin: This line imports the admin module from django.contrib. It allows you to include the Django admin site in your project.
  * from django.urls import path, include: This line imports the path and include functions from django.urls module. The path function is used to define URL patterns, and the include function is used to include other URL configurations from other Django apps.
  * urlpatterns = [...]: This is the list that holds all the URL patterns for your project. Each URL pattern is represented by an element in the list.
  * path('admin/', admin.site.urls): This line defines the URL pattern for the Django admin site. It maps the URL admin/ to the admin site, which provides an interface to manage your project's data models and perform administrative tasks.
  * path('', include('hello_world.urls')): This line includes the URL patterns from the 'hello_world.urls' module. It maps the root URL ('') to the URL patterns defined in the hello_world app. This allows you to handle requests to the root URL and delegate them to the URLs defined in the hello_world app for further processing.
6. Create a urls.py file in your app, testapp:
```
from django.urls import path
from hello_world import views

urlpatterns = [
    path('', views.hello, name='hello'),
]
```
  * from django.urls import path: This line imports the path function from django.urls module. The path function is used to define URL patterns.
  * from hello_world import views: This line imports the views module from the hello_world app. It assumes that you have a file named views.py inside the hello_world app directory, which contains the view functions.
  * urlpatterns = [...]: This is the list that holds all the URL patterns for your project. Each URL pattern is represented by an element in the list.
  * path('', views.hello_world, name='hello_world'): This line defines the URL pattern for the root URL (''). It maps the root URL to the hello_world view function defined in the views module. The name parameter is an optional argument that assigns a name to the URL pattern, allowing you to refer to it by name in other parts of your code, such as templates.

7. Restart your server or python manage.py runserver

![Screenshot (94)_WPS Photo](https://github.com/dhanvina/Django-Web-Development-Tutorial/assets/47035051/4811070b-6b67-41fd-bad1-6e4a3d0641d0)








