Write your first view

## Task

#### update the views.py 

Open the file polls/views.py and put the following Python code in it:

```
from django.http import HttpResponse

def index(request):
    return HttpResponse("Hello, world. You're at the polls index.")
```{{copy}}

This is the simplest view possible in Django. To call the view, we need to map it to a URL - and for this we need a URLconf.

To create a URLconf in the polls directory, create a file called urls.py. 


Your app directory should now look like:
```
polls/
    __init__.py
    admin.py
    apps.py
    migrations/
        __init__.py
    models.py
    tests.py
    urls.py
    views.py
```

In the polls/urls.py file include the following code:

```
from django.conf.urls import url

from . import views

urlpatterns = [
    url(r'^$', views.index, name='index'),
]
```{{copy}}

The next step is to point the root URLconf at the polls.urls module. In mysite/urls.py, add an import for django.conf.urls.include and insert an include() in the urlpatterns list, so you have:

```
from django.conf.urls import include, url
from django.contrib import admin

urlpatterns = [
    url(r'^polls/', include('polls.urls')),
    url(r'^admin/', admin.site.urls),
]
```{{copy}}

You have now wired an index view into the URLconf. Lets verify it’s working, run the following command:

Django Welcome Screen: https://[[HOST_SUBDOMAIN]]-8000-[[KATACODA_HOST]].environments.katacoda.com/polls
