- setting configuration of the project.
- its a pyhotn module with module level-variables

`ALLOWED_HOSTS = [ "www.example.com"]`
`DEBUG = False`
`DEFAULT_FROM_EMAIL = "xyz@example.in"`

- can assign settings dynamically using normal Python syntax.
`MY_SETTING = [str(i) for i in range(30)]`

- Designating the settings:
	- setting up the settings : use the DJANGO_SETTING_MODULE  environtment variable
	-  The [[django-admin]] utility:
		- using this the envrionment variable once or explicitely pass the settings module each time you run the utility. 
	`export DJANGO_SETTINGS_MODULE=mysite.settings`
	`django-admin runserver`
	- "--settings" command line argumaent to specify settings manually.
	`-django-admin runserver --settings=mysite.settings`
	- in live server environment tell the settings to use by os.environ

 `import os`
 `os.environ["Django_SETTINGS_MODULE"] = "mysite.settings"`

- **Default settings** 
	- to use the global settings, load the settings from global_settings.py

- Using settings in python
	- import the object django.conf.settings
	`from django.conf import settings`
- custom default settings
	- pass in a module or class that provides the defaults as the default_settings argument in the call to `configure()`

`from django.conf import settings`
`from myapp import myapp_defaults`
`settings.configure(default_settings=myapp_defaults,DEBUG=True)`

- It boils down to this: Use exactly one of either `configure()` or `DJANGO_SETTINGS_MODUL Not both, and not neither.
- **calling django.setup() is needed for standalone django usage.**
	- this will load the settings and populate django's application registry

`import django`
`from django.conf import settings`
`from myapp import myapp_defaults`

`settings.configure(default_settings=myapp_defaults, DEBUG=True)`
`django.setup()`


`from myapp import models`


- Types of Settings :
	- [[Core Settings]]
	- [[Auth]]
	- [[Messages]]
	- [[Sessions]]
	- [[Sites]]
	- [[Static Files]]
	- [[Core Settings Tropical Index]]

