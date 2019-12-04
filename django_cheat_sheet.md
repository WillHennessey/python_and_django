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

## Working with Models
`from blog.models import Post` - You have to import models to query them
`Post.objects.all()` - Get a queryset of all Post objects
`Post.objects.create(author=me, title='Sample title', text='Test text')` - create a Post
`Post.objects.filter(author=me)` - filter Post objects by author, this is similar to `.where` in Rails or `WHERE` in MySQL
`Post.objects.filter(title__contains='title')` - There are two underscore characters between title and contains. Django's ORM uses this rule to separate field names ("title") and operations or filters ("contains")
`Post.objects.order_by('created_date')` - order by `created_date` column this is the exact same as Rails
`Post.objects.filter(published_date__lte=timezone.now()).order_by('published_date')` - you can chain query methods together

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
