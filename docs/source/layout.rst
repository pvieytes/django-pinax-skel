Layout
======

Before we move on, I'd like to give you a quick tour of ``django-pinax-skel``'s file
layout::

.
├── LICENSE.txt
├── Procfile
├── README.md
├── fabfile.py
├── fixtures
│   └── initial_data.json
├── gunicorn.py.ini
├── manage.py
├── project_name
│   ├── __init__.py
│   ├── apps
│   │   └── __init__.py
│   ├── libs
│   │   └── __init__.py
│   ├── receivers.py
│   ├── settings
│   │   ├── __init__.py
│   │   ├── common.py
│   │   ├── dev.py
│   │   └── prod.py
│   ├── startup.py
│   ├── static
│   │   ├── README
│   │   └── css
│   │       └── project.css
│   ├── templates
│   │   ├── _account_bar.html
│   │   ├── _footer.html
│   │   ├── homepage.html
│   │   └── site_base.html
│   └── urls.py
├── reqs
│   ├── common.txt
│   ├── dev.txt
│   └── prod.txt
├── requirements.txt
└── wsgi.py

9 directories, 28 files

``fabfile.py`` is a utility script (written using `Fabric
<http://docs.fabfile.org/en/1.4.2/index.html>`_) that adds some helpful
shortcut commands. It can automatically bootstrap a Heroku app for you, and a
number of other useful things. You can run ``fab --list`` from the command line
to see its usage.

``gunicorn.py.ini`` is our `gunicorn <http://gunicorn.org/>`_ web server
configuration file. It is optimized for large scale sites, and should work well
in any environment.

``manage.py`` is our default Django management script.

``Procfile`` is our Heroku process file--which tells Heroku what our three
types of services are: ``web``, ``scheduler``, and ``worker``. To learn more
about this, see `Heroku's Procfile documentation
<https://devcenter.heroku.com/articles/procfile>`_.

``reqs`` is a directory which contains all of our pip requirement files, broken
into categories by the environment in which they're used. The ``common.txt``
file contains all of our 'shared' requirements, the ``dev.txt`` file contains
all of our local development requirements, and the ``prod.txt`` file contains
our production requirements. This modular approach is taken to make development
as flexible (and intuitive) as possible.

``requirements.txt`` is a Heroku specific file which tells Heroku to install
our production requirements *only*.

``woot`` is the base Django site. Everything inside this directory is
considered your actual Django code.

``woot/apps`` is a directory meant to hold all of your local Django
applications. If you wanted to create a ``blog`` app, for instance, you'd put
it here.

``woot/libs`` is a directory meant to hold all of your local Django
libraries--code which doesn't really fit into 'applications'. This usually
includes stuff like templatetags that are used in various place, or other
helpful utility functions.

``woot/settings`` is a directory which holds all of your Django settings files!
Much like our pip requirements, there is a settings file for each environment:
``dev.py``, ``prod.py``, and ``common.py`` (shared settings). Feel free to edit
and tweak these to your specific needs.

``woot/templates`` is a directory that holds all your Django templates. By
default, we only include a 404.html and 500.html, since those are used in all
Django projects.

``woot/urls.py`` is your standard Django urlconf.

``wsgi.py`` is your standard Django wsgi configuration file. Our webserver
uses this to figure things out :)

As you can see--everything is very straightforward. All standard Django
knowledge you have should easily apply to ``django-pinax-skel``!

.. image:: _static/yeah.png
