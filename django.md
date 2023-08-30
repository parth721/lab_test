Let's study about DJANGO

structure of django project & apps (without database setup)
<br>
```
syncall
  |---frontend
  |     |---templates
  |     |     |---abc.html
  |     |---static
  |     |     |---abc.css
  |     |     |---abc.js
  |     |---views.py
  |     |---(...)
  |---backend
  |     |---algo.py
  |     |---views1.py
  |     |---(...)
  |---syncall
  |     |---urls.py
  |     |---settings.py
  |     |---__init__.py
  |     |---asgi.py
  |     |---wsgi.py
  |     |---(...)
  |---db.sqlite3
  |---manage.py
  |---requirements.txt
venv
.gitignore
```

## MVT (Model View Template) 

* interact with DB.

* interact with receiving request, processing it & sending response to user. It also act as a mediator b/w template & model.

* It decides, how data should be represented to the user.(UI)

### Views.py <br>
The views.py file is where you write the code that processes 
* user requests, 
* performs operations on data, 
* prepares the data for rendering, 
* and returns appropriate responses to the client

```
Like in this project I created an function which take input (zipcode & countrycode) from user, make API call to get the response, from that response it collect the lattitude & longitude value. Then send that value to make another Api-call from which it collects the weather forecast data & history data of that coordinates. then only retrive the meaningful data from them & send them to algo.py to do some calculations on them & send it back to views1.py. And render them in output.html

client_request --> urls.py --> app/views.py  --> server_response
``` 

### Settings.py
it contain the info or data about project settings.

### `__init__.py `
To consider any folder as python package, which has this file.
(To know more read about "python package")

### wsgi.py 
Web server gateway interface is a specification (rule book) which tells how web app communicate with web server & other web apps to process a request.
<br>
#### it contains ?
`import os`

importing os module

`from django.core.wsgi import get_wsgi_application`

importing func.(get_wsgi_application) from wsgi module from django/core.

`os.environ.setdefault('DJANGO_SETTINGS_MODULE', 'syncall.settings')`

defining settings module to env. variable(DJANGO_SETTINGS_MODULE), by a mapping object representing the string env(os.environ)

`application = get_wsgi_application()`

obj. callable & this func. return wsgi_callable

### asgi.py
Asynchronous server gateway interface (successor of wsgi) provide std. interface b/w async-capable python web server, app, framework.

what it contain ?
