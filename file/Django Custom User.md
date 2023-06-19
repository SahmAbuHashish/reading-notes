# Reading Questions

### What are the key benefits of using a Django Custom User Model, and how does it differ from the default Django User Model?

using a Custom User Model in Django provides flexibility, data consistency, seamless integration, and future scalability. It allows you to define your own fields, behaviors, and validation rules tailored to your application's user requirements. It differs from the default User Model by offering customization options and a more tailored approach to user data management

---

### Explain the process of creating and implementing a Custom User Model in Django, including the necessary changes to settings.py and the required model fields.

Setup
To start, create a new Django project from the command line. We need to do several things:

- create and navigate into a dedicated directory called accounts for our code
- install Django
- make a new Django project called django_project
- make a new app accounts
- start the local web server

Creating our initial custom user model requires four steps:

- update django_project/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

---

### What is DjangoX and how does it complement or extend the functionality of Django? Provide an example use case for incorporating DjangoX in a project.

DjangoX is an open-source Django starter framework designed to enhance and accelerate the process of building Django web applications. It complements and extends the functionality of Django by providing a pre-configured set of tools, libraries, and features that are commonly used in Django projects. 
DjangoX aims to streamline the development workflow, increase productivity, and promote best practices by offering a well-structured project template with built-in functionalities.

- Pre-configured Components
- Bootstrap Integration
- Authentication and User Management
- Database Management
- DjangoX provides a Docker-based development environment