[Django REST Framework](http://www.django-rest-framework.org/)
===

This document are some of my notes while learning Django and Django REST Framework.


## Install Requirements
* [Xcode](https://developer.apple.com/xcode/)
* [Homebrew](https://brew.sh/)
* [Git](https://git-scm.com/)
* [Python](https://www.python.org/)
* [pipenv](https://pipenv.readthedocs.io/en/latest/)



## Getting Started
```python
# 1 - Create a Folder for your project
mkdir tutorial
cd tutorial

# 2 - Specify what version of Python you're using in this case we're using 3.6
pipenv --python 3.6

# 3 - Install Django and Django Rest Framework
pipenv install
pipenv install django
pipenv install djangorestframework
pipenv install django-cors-headers

# 4 - Enter The Virtual Environment
pipenv shell

# 5 - Create Your Django Project
django-admin startproject content .
python manage.py startapp todos


# 6 - Migrate the Database
python manage.py migrate

# 7 - Add ToDos to Installed Apps
open settings.py in the content folder
Add to INSTALLED_APPS object...
'rest_framework',
'todos',

# 8 - Create a Super User
python manage.py createsuperuser
admin
password

# 9 - Run Server
python manage.py runserver


# 10 - Check to see if it Runs
http://localhost:8000/admin/

```



## Getting Started from an Already Created Project
```python
# 1 - Clone the Repo then run...
pipenv shell

pipenv install

python manage.py migrate

python manage.py createsuperuser
admin
password

```



## Useful Commands

#### Flush the Database & SuperUser
```python
python manage.py flush
```

#### Run Migrations on Heroku after Git Push
```python
heroku run python manage.py makemigrations
heroku run python manage.py migrate
```



## Useful Links

[Heroku Django Template](https://github.com/heroku/heroku-django-template)

[DRF with React Tutorial](https://wsvincent.com/django-rest-framework-react-tutorial/)
