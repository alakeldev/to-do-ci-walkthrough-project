Frameworks:
Thinking in abstractions => 1 - Group things in categories
       2 - Analyze relationships
    Concepts and relationships can be made real in our code
    Software programs are built of concepts that are made real
    the moving parts of software machine

What is the framework goals:
a framework is a resuable "Semi-Complete" applicaton that can be specialized to produce custom applications

Frameworks:

- allow to build your application wihout haveing to worry about all the naunces that go into making your application work at the lower levels => alot of the "Plumbing" hidden
- Overcome the need for repetitive coding
- Gernerally follow the MVC pattern (Model - View - Controller)
- Used in accelerating a project's time to market
- Significantly reduce development costs in getting you there
- Written by some of the best corders in the world
- All have their own philosophy
- Manage complexity by giving us places and patterns

what are the goals of the framework?

- Reuse code, design, domain analysis and documentation (DRY)
- Simplify software development by enabling agile practices
- Reduce code writing
- Allow inexperienced designeres and programmers to develop good software
- Extract the knowledge of experienced designers and programmers

What are good development principles?
KIS => Keep it simple

- The Simpler you code is the simpler it will be to maintain it in the future
- Most Systems work best if they are kept simple rather than making them complex
- Don't rusing features from the programming language just because you can
YAGNI => You are not gonna need it
- Developers often project into the future when coding
 	- Try tp anticipate extra features that might be needed at some point
- If you don't need it now you moslt likely won't need it later
- Do the Simplest thing that could possibly work
DRY => Don't repeat yourself
- knowledge must have a single, unambiguous, authoritative representation within a system
- Do things one time, in one place rather than having the same or similar code scattered throughout your code base
 Why?
  It makes change easier later on
  Helps when it's time for maintenance

when DRY is implemented what's called Separation of concerns => the separation of concerns can also apply at heigher levels too. In OOP classes define properties , and behaviours of objects and each class should be responsible for one and only one thing, such as : display a video , pay a bill, monitor a heartbeat.......
no wether classes on the system should have a duplicate responsibility ...why? because it gets messy and confusing

Separate:

- User interface
- Datastore access
- logic that communicates between UI and datastore

Well known pattern: => MVC pattern

What is a pattern?
a written document describes a general solution to a design problem that recurs repeatedly in many projects

- Software desginers adapt the pattern to their specific projects
no one such pattern used at the heart of most frameworks is a model view controller MVC pattern so MVC is an architectural programming paradigm and it's used by many web frameworks, also a way of thinking and processing information
Important to focus:
it's a way to structure your application
it's a way of working with data in its three mainfestations:
data at rest => model           SQL
data in motion => controller    Python
data as presented => view       HTML

Frameworks implement the MVC pattern, but the pattern is not a framework
Frame works are popular because of MVC

MVC goals:
1 - promote code resuability
2 - separation of concerns
 the goal of MVC and related patterns is to separate data management and presentation
  by breaking application down into smaller more discrete and easier to manager components

MODEL:
Model represents persustent data accessed from or ti be written to some data store.
The Model represent the data you are working with, also the models are part of the application implement the logic for the application's data domain

Often Model code retireves and stores data in a database, for example a product model object might retrieve information from database operate on it and then write update information back to a products table in a database.
The Model might have direct aceess to the database or it may access to some data service via an API.

VIEW:
views are comprised of HTML, CSS and other elements that make up the look and feel of an application
Views are the components that display the application user interface or UI. they are often constructed as templates with placeholders for data to be injected to them for display on your screen typically this UI is populated from the model data. an example would be an edit view of a product table that displays text boxes, drop down lists, and check boxes, with data based on the current state of a product object.

CONTEROLLERS:
That's the code that does the thinking and decision making. controllers are components that handled user interaction, they work with the model and ulimately select a view to render that displays UI.

In an MVC application the view only displays information that the controller handles and responds to you in response to user input and interaction, for example the controller handles query string values in the URL and passes these values to the model which in turn, might use these values to query a database.

Summary:
Model: is used for adding and retrieving data from a database or other structure, it talks only to the controller, no contact with the view.

View: Can consists of templates it's the only thing that the user sees, and it it talks and listens to only to the controller and generally it invloves HTML and CSS.

Controller: never talk to the database directly only to the model, the model responsbile for fetching the data and exit, it never talk to the screen directly eighter only to the view. so the event handling process such as get, put, delete. these are all requests in the view and they are processed by the controller.

Every application needs some structure expecially the more complex ones, MVC helps you stay organized from start to finish, you often end up writing less code not more, and slo there is a shallower learning curve as your project grows

Server Side Frameworks:
it Cassified as either full frameworks or Micro Frameworks
the difference between the two depends on how much low-level automation the framework is capable of.
How many batteries for example: pre-install components come with the framework?

Django:
What does Django look like?
In Django the MVC view is called the template (MVT)
The MVC model is still the model
But the MVC Controller is called the View in Django
So the Template is the user interface
the model is still the model
and logic livers in views

ORM => Object Relational Mapping

Django Behaviour:
Browser => URLS => Views => Models => Database

Database => Models => Views => Templates => display on your browser





# Django Section Importan Information and commands:
- Django is an open-source web framework for building robust and dynamic web applications with ease.
- Django Project => serves as the top-level container for your web application. It encompasses everything related to your application, including settings, URLs, database configurations, and more.
- Django Applications =>  it is a Python package that provides a specific set of features. Applications are wired into projects using the INSTALLED_APPS setting in the project’s settings.py. This setting specifies which applications are part of the project.

General Commands and information that can be used with any django project

Installing packages:
pip install django
pip freeze --local > requirements.txt


Create django project:
django-admin startproject project_name .    => the dot at the end tells that the project should be created in the current directory
py manage.py runserver  => within this process you can open the browser and take the url (host name) and past it inside project_name/settings.py => ALLOWED_HOSTS = [' HERE PAST IT like 127.... ']


Create django apps:
py manage.py startapp app_name


Create views:
Go to: app_name/views.py


Create URLs: 
Go to: project_name/urls.py
You must setup the main urls for your project and for the apps too there (project_name/urls.py) - then you can move and go to inside each app and modify its urls.py for each view and page.


Create models and define the DB structure:
Go to: app_name/models.py within this file stored the DB models and define the structure of the DB used by our app


Add apps to your project:
Go to: project_name/settings.py

INSTALLED_APPS = [ 
       "HERE YOU CAN ADD YOUR APPs",
       "HERE YOU CAN ADD YOUR APPS",
       
]

also inside the settings.py another settings to set like secrit key , db connection.


* manage.py file is in the root directory, above the project folder. It's used to create apps, run the project and preform some DB options.


Create DB table:
py manage.py migrate


apply the changes on table fields through run:
py manage.py makemigrations
py manage.py migrate


Craete DB admin:
py manage.py craetesuperuser



very important file to check for any new django project:
["Django Full Instrunctions"](https://docs.google.com/document/d/17E5_Ya9WDmsoZmRAWu1fUmRIXcdj18zTopERHX9KTOA/edit?fbclid=IwAR2QRLtmOdn3g1fcI7StG8xuzDO64w2ej6gVn8W3JDrEMd8jRV8CiMUTpNk)




-------------------------------------------------------------------------------------------------------------------------------------------------------
### Some commands that related to the todo project:

py -m django startproject django_todo



python manage.py startapp todo



 python manage.py makemigrations --dry-run     (--dry-run) => it's a flag to show us the command steps so in the future run it without this flag


 python manage.py showmigrations


 python manage.py migrate --plan                (--plan) => it's a flag to show us the commad what is going to do



 python manage.py createsuperuser      








pip install coverage


python -m coverage run --source=todo manage.py test




python -m coverage report




python -m coverage html
