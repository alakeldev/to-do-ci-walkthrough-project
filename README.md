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
- Extract the knowledge of experienced designers and programmers and they have their basic properties as well. So what are they?
       The basic properties are:  [modularity, reusability, extensibility, inversion of control, and non-modifiable code].

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

dealing with a dry rule. So a good programmer is a lazy programmer, that thinks
things through they'll build it once and reuse it again. So let's look at an
example, you might be involved in building a large software project.
You will initially be overwhelmed by the overall complexity, because we
humans are not good at managing complexity. What we are good at is finding
creative solutions for problems that are small chunkable manageable units. And a
basic strategy for reducing complexity, to these manageable units is to divide a
system into parts that are more easily tackled. You might first want to divide
your system into components, where each component represents a subsystem that
contains everything needed to accomplish some specific
functionality. For example, if you're building a web application that includes
membership, a blog, maybe a forum, some kind of payment system and
administration area, you might chunk each of these features into components.
The membership component, could be divided into say smaller sub components
like role management authorisation and authentication. When we divide systems
into components and subcomponents we eventually arrive at a level where the
complexity is reduced to a single responsibility. These responsibilities
can sometimes be implemented as single functions. At this level, the problems
become easier to solve and the result can be a clean well thought-out solution
that can be understood and reused again in later projects.
That solution represents the responsibility. It can communicate with other islands of
responsibility, that it can turn communicate with other islands
themselves, to compose an overall solution to the more abstract high-level
problem that the project is trying to solve in the first place.
The DRY principle insists that each Island of responsibility is unique in what it does.
What emerges when DRY is implemented what is what call is what's called a
separation of concerns. The separation of concerns can also apply at
higher levels too. In object-oriented programming, classes define properties
and behaviors of objects and each class should be responsible for one and only
one thing. That thing might be to display a video, pay a bill, monitor a heartbeat,
open a door, or even turn off a light. No other classes in a system should have
a duplicate responsibility. Why? Well because it gets messy and confusing.
Which class do I work with to turn off the light? If I modify the behavior in
one class do I need to modify this similar class too? We can further scale
up the notion of separation of concerns and DRY to an even higher level. We can
separate the user interface component of a system from the parts that access a
database. We can then separate out the part the part of the subsystem that
communicates between the UI and the database. This separation takes the
form a well-known pattern, that pattern is called Model View controller or the
MVC pattern, and that's what we look at next.

when DRY is implemented what's called Separation of concerns => the separation of concerns can also apply at heigher levels too. In OOP classes define properties , and behaviours of objects and each class should be responsible for one and only one thing, such as : display a video , pay a bill, monitor a heartbeat.......
no wether classes on the system should have a duplicate responsibility ...why? because it gets messy and confusing

Separate:

- User interface
- Datastore access
- logic that communicates between UI and datastore

-----------

Well known pattern: => MVC pattern

What is a pattern?
a written document describes a general solution to a design problem that recurs repeatedly in many projects

- Software desginers adapt the pattern to their specific projects
no one such pattern used at the heart of most frameworks is a model view controller MVC pattern so MVC is an architectural programming paradigm and it's used by many web frameworks, also a way of thinking and processing information
Important to focus:
it's a way to structure your application
it's a way of working with data in its three mainfestations:
data at rest => model           SQL |
data in motion => controller    Python |
data as presented => view       HTML |

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

Every application needs some structure expecially the more complex ones, MVC helps you stay organized from start to finish, you often end up writing less code not more, and slo there is a shallower learning curve as your project grows.

----------------------------------------------------------------

Server Side Frameworks:
it Cassified as either full frameworks or Micro Frameworks
the difference between the two depends on how much low-level automation the framework is capable of.
How many batteries for example: pre-install components come with the framework?
Now let's look at server-side frameworks, well server-side frameworks can be
classified as either full or micro. The difference between the two depends on
how much low-level automation the framework is capable of.
How many batteries for example, pre-install components come with the framework?
Well full frameworks are chock full of pre-installed components and low-level
automation, while the micro frameworks as you might imagine come with less bells
and whistles. There are pros and cons to each framework type. So what are the pros for a full one?
For example, like Django. Well you get many batteries included, there's lots
of lower-level automation, for example, object relational mapping.
The cons of full frameworks are their larger size, their less flexible
than micro because of the large structure, and it also becomes more
opinionated. So what are the pros of small ones? Something like flask, for
example. Their small size, they have an initial shallower learning curve and
they're very flexible to customisation. But the cons of this is there aren't as
many batteries included as a full. There's less automation provided and the
automation becomes steadily more complex when additional customisation is
required due to the lack of these pre-built components. So choosing one
particular framework for your project depends heavily on the project's requirements.
Smaller projects or projects that require a lot of
flexibility and customisation, they typically used micro frameworks.
Developers often use full frameworks for large projects that don't require much
low-level framework customisation. So let's look at Django as a full framework.
Well Django is a powerful full server-side framework written using Python.
So when you're out in the world working as a developer you're going to
have to work to a schedule and hit deadlines, which are always tighter
than you'd like. You're probably going to find that each project can have a common
core set of issues. In addition to project specific ones, well what you need
is a collection of tools that can take care of a lot of the heavy lifting so
you can focus on the bigger picture. Well this is where Django and a lot of other
frameworks as well come in. But as the Django
Software Foundation put it, Django makes it easier to build
better web apps, more quickly and with less code, so you can focus on writing
your app without needing to reinvent the wheel.
So why Django, why choose it? Well it's a mature framework, it's been around since
about 2003. Django was originally developed as an in-house framework to
manage a series of online news websites, and Django grew organically
from real-world applications written by a web development team in Kansas in USA.
When web programmers at the Lawrence Journal World newspaper began using
Python to build applications. The world online team who were responsible for the
production and maintenance of several local news sites. Well they thrived in a
development environment dictated by journalism deadlines. There were three
online newspapers owned and supported by the team there was the LJ World.com. there
was Lawrence.com and cavesforce.com. The journalists on the team demanded the
features be added an entire applications be built on incredibly short deadlines.
Sometimes stuff had to be built or added even within hours. So in an attempt
to avoid repeating themselves and building the same stuff over and over
again. The developers set about building a framework that suited their needs
under such pressure. They called a framework Django after their shared love
of the jazz guitarist Django Reinhardt. So, two years later the source code was
then released publicly, on the net, and the Django team carried on with the
development and contributing to the open-source model.
Because Django was created in a news environment it has built-in features that are very suitable
to content management. Such as an administration interface where
developers and users can add and edit content and elements through a backdoor
interface available only to authorised users. Most data-driven web applications
will require some kind of administration screens to add and modify data whether
that data includes registered users on the site or products being sold.
In keeping with its DRY philosophy, Django allows you to administer your
model data through the webpage courtesy of the administration module.
This saves you from having to build your own from scratch. And to enable the existence of
authorised and authenticated users Django also comes with pre built
authentication functionality. But don't think that Django is limited
just to content management. It's much more powerful and flexible than that.
Django has steadily become a favorite amongst the Python development community.
Currently Django sites.org lists nearly 5,000 sites built with this
framework. The most famous of them being Pinterest, Instagram, and Discuss.
So EDX, for example, the massive open line online community course is developed jointly by
Harvard and MIT is also developed by Django.
What's more the edx is now open source and there are over 70 companies
contributing to its development. So there's a ton of pre-built functionality
available to anybody wanting to use this platform. And because it's a free full
stack framework Django serves is the perfect starting point if you're new to
web frameworks. Django's documentation is rich and mature which is a major plus
for anyone trying to tackle the intricacies of a data-driven project often
for the first time. Also, Django's admin interface is great for
data entry and testing during the early stages of a project. So, to quote the
official website in Django project.com, Django is a high-level Python web
framework that encourages rapid development and clean pragmatic design.
It's built by experienced developers, it takes care of much of the hassle of web
development, so you can focus on writing your app without needing to reinvent the wheel
it's free and it's also open source.

------------------------



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

Now what does Django look like? Well Django has built-in tools that are set
up to create projects. In Django a project is a container for your site, a
project is really just a collection of apps. And an app is a self-contained
piece of functionality that contributes to your site as a whole. For example, an app
might be a payment system, or a blog, or a forum. Apps are similar to modules in a
content management system, CMS, but they tend to be a lot more smaller in scope.
And they typically perform only one main function. This allows for the development
and maintenance of a site at a more granular level. Individual apps can be
modified or swapped out for other apps. All done in relative isolation
from the functionality contained in other apps, separation of concerns.
Multiple developers can work on the site via apps without corrupting each other's code.
So for example, imagine you were building a Facebook clone. You might
create a project called, the social, for example. Well take a moment to consider
the structure you would deploy in Django, for example. For instance, the site might
may contain apps like messaging, timeline ratings, some kind of info wall, adding
friends, upload media, etc. All of which contribute to the overall site experience and functionality.
These apps can be built and maintained separately from each other,
but are all controlled from the project. Angular also adheres
a variation of the MVC pattern. So Django projects are logically organised around
the MVC pattern or the MVC architecture. However, Django MVC architecture is
slightly different, in that the views also act as controllers, more on this.
At a high level Django is organised in a variation of
the MVC pattern, known as the MVT model view template. Is this is confusing?
Possibly, but there are different flavors of MVC that can be head scratching but in
Django the MVC view is called the template. The MVC model is still the
model but the MV controller is called a view in Django. So the template is the
user interface, the model is still the model, and the logic
lives in views. Okay let's look at models in Django. Well Django works brilliantly
with databases, the framework can take developer defined Python classes and
known as models, and automatically create database tables and their relationship for us.
So also any changes to our models can be automatically reflected in our
database schemas, its all automated. This pattern is known as object relational
mapping, ORM. A model is a single definitive source of information about
your data, it contains the essential fields and behaviors of the data you're storing.
Generally each map model maps to a single database table. To quickly get
you up and running, Django comes with the SQLite database for development and
testing. Although, I worked on a specialist project where a SQLite was
used in production in general it lacks the power and functionality of say MySQL
or Postgres, either which can be easily swapped in when deploying your project
to a live or production environment. Like other full-stack frameworks such as
Ruby, on Rails, or asp.net, MVC, and spring, etc. Java, spring, etc.
Django adheres to the philosophy of convention over configuration. This means that a
developer need only specify the unconventional aspects of the
application. For example, if there's a class called blog in our model or code,
the framework will create a corresponding table in the database
called blog by default. It's only if you stray from this convention, such as
calling the table the blog table, that you need to explicitly write the code to
do that. This implicit functionality is an example of hiding the plumbing that
we touched upon earlier. Bear in mind though, that for the Python purists this
breaks the Zen of Python decree that explicit is better than implicit. That is
Pythonista's say it's better to see the code it does something rather
than having it hidden from the developer. Well, why? Well because when it comes to
fixing or improving behavior it's easier to do this when the behavior is right
there in your code. It's one of the downsides of having bells and whistles
and batteries in your framework.
Django also has templates, so this is the presentation layer that defines how
information is displayed to the end-user. They visually represent the data model,
the template layer provides a designer friendly syntax for rendering the
information to be presented to the user. So what is the template philosophy?
So business logic should be separated from the presentation logic, templates are
only concerned with presentation of data and other visual elements.
It's impossible to call Python code directly within Django templates.
Templates syntax should be decoupled from HTML and designers assumed to be comfortable with
HTML and JavaScript code. Designers are assumed not to be Python developers.
Although, templates do accommodate small teams in which the templates are created
by Python programmers. The syntax, template syntax is embedded within
normal HTML and is used to inject data into a web page. The most common template
language used is the Django template language. Although another templating
language such as Jinja 2 for example can be used with most python-based
frameworks, including Django. In the example, in the template examples shown
here, we are looping through a list of colors and displaying a HTML list of each
coders name. Now the goal of a template language is not to invent a full-blown
programming language. The goal is to offer just enough programming ish
functionality such as branching and looping, that allows us to make a GUI
related decisions. So let's have a look at the views, for example. Now in Django,
views define the business logic that link the templates and the models. Here's
what happens when a visitor lands on your Django page, for example.
So first, Django consults the various URL patterns that you've created and uses
that information to retrieve a view. The view then processes the requests,
querying your database via the models if it's necessary, the view then passes the
request information onto your template. The template then renders the data in a
layout you've created and displays it on the page so down it and back up.



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




## Deplay process:


You learned the different settings that were required prior to deployment, and took a deeper
dive into the settings.py and requirements.txt files.
In this video, we will review the deployment flow including the use of the Procfile, before
leaving you with some key takeaways from the lesson.
First, let’s consider what happens when we deploy to Heroku for a moment.
We deployed our simple project by creating a Heroku app - not to be confused with a Django
app - and attached our GitHub repository to it.
During the deployment, Heroku cloned the repository and determined that our project was written
in Python.
As a result, it started to process the requirements.txt file to install the packages we need.
Heroku then examined the Procfile.
If you remember, the Procfile is in this format: process type : command
In our case, we stated that the process type was web.
This specifies that we are running a web application.
There are other process types, but web is the most common.
The command is what we would type to run the project.
When we run it in the terminal, we type python3 manage.py runserver
You could put that command in the Procfile too if you want.
The reason we use gunicorn to run the project is that it is a more robust and scalable,
production-ready server.
You may be curious about what my_project.wsgi means.
Each directory in our Django project is actually a Python package.
So, my_project.wsgi means the wsgi module in the my_project package.
If you have a look in the my_project directory, you will see a wsgi.py file.
That is what is being referred to.
WSGI, which - to my delight - is pronounced whiskey, stands for Web Server Gateway Interface.
It was created to allow web servers to communicate with Python web frameworks in a uniform, consistent
way.
When the repository is cloned, the requirements are installed and the Procfile is in place,
Heroku knows exactly how to run our project.
The key points we would like you to remember from this lesson are:
Deploy early and regularly Add, commit and push your code to GitHub regularly
Recreate your requirements.txt file after every new package is installed
Always switch DEBUG to False in your deployed project
In this lesson, we have learned how to deploy a Django project to Heroku and we have looked
in detail at the settings.py and requirements.txt file.
In this video, we have looked at the deployment flow and demystified the Procfile.
Now, proceed on to the quiz before we begin building a full-featured Django project.

python -m coverage html
