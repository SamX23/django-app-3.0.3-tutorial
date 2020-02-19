# This is my progress learning Django framework based on the tutorial in djangoproject.com

# Requirement
- Python
- Django Framework
- VScode
- Bash

# Views or page
- Question “index” page – displays the latest few questions.
- Question “detail” page – displays a question text, with no results but with a form to vote.
- Question “results” page – displays results for a particular question.
- Vote action – handles voting for a particular choice in a particular question.

# Steps-command
- django-admin startproject (directory) . // using (.) if creating project on existing directory
- python manage.py runserver (port) // port is optional
- python manage.py startapp (name folder/app) #this can be said as a home directories
- Setup Views, URL, timezone, setting
- python manage.py migrate // create table based on setting
- Setup models and activate in setting
- python manage.py makemigrations (apps) // Create migrations for changes
- python manage.py sqlmigrate (apps) 0001 // Creating database and retuns SQL
- python manage.py check // to check any database problems in project
- python manage.py migrate // to migrate again after changes
- python manage.py shell // interactive django with env variable to plays with API
- python manage.py createsuperuser // create admin
- Finished - Customize, test and release.

# Test and squashing bugs
- adds test.py in home directory
- python manage.py test (app)

# Test a view
- Python shell
 from django.test.utils import
 setup_test_environment
 setup_test_environment()
 from django.test import Client // create an instance of the client for our use
 client = Client()
 response = client.get('/') get response from ('/')
 response.status_code
 from django.urls import reverse
 response = client.get(reverse('(app):index'))
 response.status_code
 response.content
 response.context['latest_question_list']
