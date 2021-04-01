# Simple Django Cookiecutter

Quickly build a new Django project choosing default preferences.

Default projects have:
  * Common file hiearchy
  * Python 3.8 or higher
  * Django 3.1 or higher
  * Django Bootstrap
  * Django Environ (12 Factor App)
  * Whitenoise to serve static files
  * Sitemap for dynamic Sitemaps
  * Django Debug Toolbar (development dependency)
  * Modern TOML file project format (vs setup.py)

## Create project soruce code

1. `git clone https://github.com/glenjarvis/django-cookiecutter-glenjarvis.git`
2. Answer questions about project
3. `cd <project_slug>/src/django_website/<project_slug>`
4. `mv env_example .env`
5. `cd ../../../`  You should now be in the top of the newly created porject
6. `git init`

## Activate Python environment

Create / Activate an isolated Python environment for your project however you
prefer.
For example:

1. `python3 -m venv venv`
2. `source venv/bin/activate`
3. `pip install --upgrade pip`

## Install library dependencies

Install the requirements for the project however you prefer.

For example:

1. `pip install poetry`
2. `poetry update`
3. `poetry export --without-hashes -f requirements.txt -o requirements.txt` 

Note: The top level Make file has a `make reqs` for reguarly exporting poetry
requirements into `requirements.txt`. This helpful for those not familiar who
who prefer not to use poetry for dependency management

## Configure Initial Django

1. `cd src/django_website`
2. `./manage.py migrate`
3. `./manage.py createsuperuser`
4. `./manage.py runserver`

