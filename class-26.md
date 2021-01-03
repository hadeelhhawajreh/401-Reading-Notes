### Getting started with Django


Django is a free, open source framework, written in Python, where projects follow the Model-View-Template structure (usually shortened to MVT). Django emphasizes reusability of components as well as rapid development, as well as the principle of non-replication. 

Python is used in all aspects of this framework, such as settings, database models, etc. 

The most popular sites that use Django are: Pinterest, Instagram, Mozilla, The Washington Times, Disqus, National Geographic and many more. 

Django was developed in 2003 by programmers Adrian Holovaty and Simon Willson, who work for Lawrence Journal World, when they moved to Python to build applications. Django was launched in 2005 under a BSD license


MVT architecture
Django's project structure is divided into three sections that are linked to each other, but are different from other frameworks that follow a structure (MVC-Model, View, Controller) such as Laravel in PHP and others, where projects in Django consist of model model, View view, and template template. 

The model section processes, handles, and retrieves data, and Django supports many databases, such as: SQlite, MySQL, and PostgreSQL. 
A display is a collection of Python functions that respond to a particular URL, and the display function is to determine which data and information to display. 
A template is an HTML file in which you determine how the information displayed in the display section will appear. 
So where's controller? The controller here is the framework itself, the mechanism by which the request is sent to the appropriate view based on a specific URL.
