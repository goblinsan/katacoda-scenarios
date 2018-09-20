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

Ok, try and run the project.  We'll start the server in a separate terminal so we can leave it running.

We're running in a virtual shell so we need to open that env in the 2nd terminal then start the server:
```
cd /home/scrapbook/tutorial
pipenv shell
cd /home/project/
```{{execute T2}}

`python manage.py runserver 0.0.0.0:8000`{{execute T2}}

If you want to shut it down, just use: <kbd>control</kbd> + <kbd>c</kbd>

### Can you see it?

Django Welcome Screen: https://[[HOST_SUBDOMAIN]]-8000-[[KATACODA_HOST]].environments.katacoda.com 

### Probably not...
You probably see something like this:
```
DisallowedHost at /
Invalid HTTP_HOST header:...
```

So let's update the ALLOWED_HOSTS setting.

### Open the Theia editor in the IDE tab
In your project settings.py file,set ALLOWED_HOSTS to this (line 28) :

`ALLOWED_HOSTS = ['[[HOST_SUBDOMAIN]]-8000-[[KATACODA_HOST]].environments.katacoda.com', '[[HOST_IP]]']`{{copy}}

### Now can you see it?

Django Welcome Screen: https://[[HOST_SUBDOMAIN]]-8000-[[KATACODA_HOST]].environments.katacoda.com 

