# TA Portal ![Status active](https://img.shields.io/badge/Status-active%20development-2eb3c1.svg) ![Django 2.0.5](https://img.shields.io/badge/Django-2.0.5-green.svg) ![Python 3.6](https://img.shields.io/badge/Python-3.6-blue.svg)
[![Build Status](https://travis-ci.org/devlup-labs/ta_portal.svg?branch=master)](https://travis-ci.org/devlup-labs/ta_portal)
## A platform for automating the task of generating reports of work done by Teaching Assistants

### Installation:
Requirements:
- Python 3.6 runtime
- Django 2.1
- Other dependencies in `Pipfile`

Procedure:
- Install [python](https://www.python.org/downloads/) in your environment(pre-installed on Ubuntu).
- Navigate to the cloned repository.
    ```
    cd <project_directory_name>     # ta_portal
    ```
- Install `pipenv` for dependency management
    ```
    pip install pipenv
    ```
- Use pipenv to install other dependencies from `Pipfile`
    ```
    pipenv install --dev
    ```
- Copy `.env.example` to `.env`
    ```
    cp .env.example .env
    ```
- Change to `src` directory and optionally activate virtual environment, if you don't want to activate env, use `pipenv run` to run python scripts
    ```
    cd src
    source "$(pipenv --venv)"/bin/activate
    ```
- Make database migrations
    ```
    python manage.py makemigrations --settings=ta_portal.settings
    python manage.py migrate --settings=ta_portal.settings 
    ```
- Create a superuser
    ```
    python manage.py createsuperuser --settings=ta_portal.settings 
    ```
- Run development server on localhost
    ```
    python manage.py runserver --settings=ta_portal.settings 
    ```
