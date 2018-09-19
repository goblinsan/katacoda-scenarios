Creating your first app

## Task

#### Creating the Polls app 

Before we start. Shutdown the running sever so we can build the app files:
<kbd>command</kbd> + <kbd>c</kbd>

Your shell should be in /home/project
`pwd`{{execute}}

If not, cd there:
`cd /home/project`{{execute}}

Now create the Polls app

`python manage.py startapp polls`{{execute}}

That’ll create a directory polls, which is laid out like this:

```
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    views.py```