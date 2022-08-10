Docker is really just Linux containers which are a type of virtualization.

Virtualization has its roots at the beginning of computer science when large, expensive mainframe computers were the norm

is what Docker is. A way to implement Linux containers!

An analogy we can use here is that of homes and apartments. Virtual Machines are like homes: stand-alone buildings with their own infrastructure including plumbing and heating, as well as a kitchen, bathrooms, bedrooms, and so on.

Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.




Containers vs Virtual Environments

If you are a Python programmer (like me) a common question at this point is, what about virtual environments? How do they differ from containers?

Virtual environments are used to isolate Python software packages locally. We can create an isolated box for individual projects so one can use Python 2.7 and Django 1.5 while another can use Python 3.5 and Django 2.1 on the same computer. Virtual environments are great.

But…virtual environments can only isolate Python packages. They still rely on a global, system-level installation of Python albeit they can refer to the proper version. So when we use Python 2.7 in a project, we’re pointing to an installation of Python 2.7 on the computer itself, not actually within the virtual environment.

Also we can’t run a production database or other services within virtual environments so compared to Docker containers they are far more limited




Docker is a way to run Linux containers
Containers are a lightweight alternative to Virtual Machines
Dockerfile is a list of instructions for creating an image
Images are made up of one or more layers
Containers are a running instance of an image
docker-compose.yml controls how to run the container
Containers are stateless and ephemeral in nature. We can link the local filesystem via volumes but things become more complex with databases

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework. It always must be added to a project after Django itself has been installed and configured.




Traditional Django

Navigate to the existing code directory on the Desktop and make sure you are not in a current virtual environment. You should not see (.venv) before the shell prompt. If you do, use the command deactivate to leave it. Make a new directory called library, create a new virtual environment, activate it, and install Django.




each app has a __init__.py file identifying it as a Python package and there are 6 new files created:

admin.py is a configuration file for the built-in Django Admin app
apps.py is a configuration file for the app itself
migrations/ is a directory that stores migrations files for database changes
models.py is where we define our database models
tests.py is for our app-specific tests
views.py is where we handle the request/response logic for our web app
Git

Whenever we have added new code it is a good idea to track our progress using Git. Make sure you’ve stopped the local server with Control+c. Then run git init to initialize a new repo and git status to check its contents.