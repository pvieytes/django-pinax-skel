django-pinax-skel
=================

A modern Django (1.4) project skeleton.


Purpose
=======

For background, see: http://rdegges.com/deploying-django and http://pinax.github.com

Essentially--deploying Django projects is hard. There are lots of things you
need to take into consideration. Being a Django user for years, I believe I've
found some extremely useful patterns to help manage all sorts of Django sites
(from the very smallest apps, to the largest).

This project is meant to be a boilerplate project for starting development. It
is heavily opinionated in terms of services and tools--but I think the tradeoff
is worthwhile.


Install
=======

django-pinax-skel currently supports Django 1.4. To create a new django-pinax-skel base
project, run the following command (this assumes you have Django 1.5 installed
already):

    $ django-admin.py startproject --template=https://github.com/tjetzinger/django-pinax-skel/zipball/master woot
    $ heroku config:add DJANGO_SETTINGS_MODULE=woot.settings.prod


Where ``woot`` is the name of the project you'd like to create.

This is possible because Django 1.4's ``startproject`` command allows you to
fetch a project template over HTTP (which is what we're doing here).

While not strictly required, it is also recommended to do

     $ heroku config:add SECRET_KEY=putsomethingfairlycomplexhere

The production settings pull SECRET_KEY from environment but fallbacks
to a value which is generated mainly for development environment.

This setup allows you to easily keep your site in a public repo if you so 
wish without causing opening a route to attack your Django passwords.
