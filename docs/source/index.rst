django-pinax-skel
===========

*A modern Django 1.4 project skeleton.*

.. image:: _static/skel.jpg

Django is a great framework. Unfortunately, like any framework, it is only as
useful as the tools you use with it. This is where ``django-pinax-skel`` *really*
shines.

``django-pinax-skel`` gives you a great project skeleton, complete with:

* Database migrations via `South <http://south.aeracode.org/>`_.
* Static file management via `django-compressor <http://django_compressor.readthedocs.org/en/latest/index.html>`_.
* Task queueing via `Celery <http://celeryproject.org/>`_.
* Helper utilities for working on the command line, via `Fabric <http://docs.fabfile.org/en/1.4.2/index.html>`_.
* Fancy documentation generation via `Sphinx <http://sphinx.pocoo.org/>`_.
* Awesome local debugging and analysis via `django-debug-toolbar <https://github.com/django-debug-toolbar/django-debug-toolbar>`_.
* Amazon S3 integration (for publishing static assets: css, js, images, etc.) via `django-storages <http://django-storages.readthedocs.org/en/latest/index.html>`_.
* CSS compression (for production environments) via `cssmin <https://github.com/zacharyvoase/cssmin>`_.
* JS compression (for production environments) via `jsmin <http://pypi.python.org/pypi/jsmin>`_.
* Memcache caching support via `django-heroku-memcacheify <https://github.com/rdegges/django-heroku-memcacheify>`_.
* PostgreSQL support via `django-heroku-postgresify <https://github.com/rdegges/django-heroku-postgresify>`_.
* A blazing fast WSGI server for serving production traffic via `gunicorn <http://gunicorn.org/>`_ and `gevent <http://www.gevent.org/>`_.
* Production application performance monitoring and usage statistics via `newrelic <http://newrelic.com/>`_.
* All the best practices I've come to learn with more than 4 years of Django
  experience.
* Built in support for production deployments on `Heroku's <http://www.heroku.com/>`_
  platform.
* Python interpreter for Linux, BSD, OS X and Windows via `bpython <http://bpython-interpreter.org>`_.
* Reusable, generic mixins for Django via `django-braces <http://django-braces.readthedocs.org/en/latest/index.html>`_.
* Django model mixins and utilities via `django-model-utils <https://github.com/carljm/django-model-utils/>`_.
* Management Extensions via `django-extensions <http://pythonhosted.org/django-extensions/>`_.
* Logging utilities via `logutils <http://pythonhosted.org/logutils/>`_.



But, more importantly, ``django-pinax-skel`` gives you a really clean, simple, and
reliable project template for developers of any experience level.

If you want a best practices approach to Django, use ``django-pinax-skel`` and you
won't be disappointed!


Follow the Guide Below to Victory!
----------------------------------

.. toctree::
    :maxdepth: 2

    prerequisites
    getting-started
    layout
    developing
    running-on-heroku


Also...
-------

Need help? Got a question? Want to post random pointless comments? Head over to
our `GitHub issue tracker <https://github.com/tjetzinger/django-pinax-skel/issues>`_ and
leave a message!

Wanna just hang out with some other bad-ass hackers like yourself? Say hi on
`#heapify <irc://irc.oftc.net/#heapify>`_, or you could follow me on `twitter
<https://twitter.com/#!/rdegges>`_.
