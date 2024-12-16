- **Create Views As Classes ,link them to url, 


- install Django
	- `python3 -m pip install django`
- creating project 
	- make directory named after the project :
		- `mkdir example`
	- bootstrap a new project  [[Start project]]
		- `django-admin startproject mysite djangotutorial`
		
	- run server to verify
		- `python3 manage.py runserver`
	- enter the same directory as manage.py and use startapp
		- `python3 manage.py startapp polls`
		- that will create a file system like this :
						- `polls/`
			    `__init__.py`
			    `admin.py`
			    `apps.py`
			    `migrations/`
			        `__init__.py`
			    `models.py`
			    `tests.py`
			    `views.py`
	- Writing View:
		- open the polls/views.py :
			- `from django.http import HttpResponse`
			- `def index(request):`
				- `return HttpResponse("hello world")`
	- to define a URL config for the polls app:
		- create a file polls/urls.py with code
		`from django.urls import path`
		`from .import views`
		`urlpatterns = [`
			`path("",views.index,name="index"),]`
	- 