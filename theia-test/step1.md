Setting up Django

## Task

#### First we'll setup pipenv and then run those commands in that shell 

We'll run these commands in the tutorial directory:
`cd /home/scrapbook/tutorial`{{execute}}

Install pipenv:
`pip install pipenv`{{execute}}

Open the available shell:
`pipenv shell`{{execute}}

Install Django:
`pipenv install django`{{execute}}

Once Django is installed we can use it to generate a project structure for us.  This time we'll create it in the Theia project directory:
`cd /home/project/`{{execute}}
`django-admin startproject mysite /home/project`{{execute}}

Ok, try and run the project:
`python manage.py runserver 0.0.0.0:8000`{{execute}}

Can you see it?
Django Welcome Screen: https://[[HOST_SUBDOMAIN]]-8000-[[KATACODA_HOST]].environments.katacoda.com 

You may see some UNKNOWN-HOST errors... in which case update your settings.py

`hostname -i`{{execute}}

In your project settings.py file,set ALLOWED_HOSTS like this :

ALLOWED_HOSTS = ['localhost', '127.0.0.1', '2886795266-8000-kitek01.environments.katacoda.com', '172.17.0.2']

Next, start your first app by running python manage.py startapp [app_label].

python manage.py startapp polls
