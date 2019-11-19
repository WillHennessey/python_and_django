# Django Cheat Sheet

## General setup commands

`mkdir my_project` - create project directory

`python -m venv my_env` - create your own virtual env for the project (python3 for mac/linux)

`my_env\Scripts\activate` - loads your env (my_env is the name of your env)

`python -m pip install --upgrade pip` - upgrades pip to the latest version

`pip install -r requirements.txt` - pip install all packages specified in the requirements.txt file (poor man's Gemfile)


## Management commands
`python manage.py startapp blog` - create an app inside the project ("blog" is the appname)

`python manage.py makemigrations blog` - generates a migration file based off the blog models

`python manage.py migrate blog` - run the migrations for the blog app

`python manage.py createsuperuser` - creates a superuser


## Config File Examples

#### Typical `.gitignore` file
```
*.pyc
*~
/.vscode
__pycache__
myvenv
db.sqlite3
/static
.DS_Store
```

#### Typical `requirements.txt`

```
Django~=2.2.4
```
