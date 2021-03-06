Installation
------------

Django-QA aims at keeping things simple. To install it you have to do what you would do with most django apps.

Install with pip::

    pip install django-qa

Add qa and its requirements to INSTALLED_APPS in your project settings:

.. code-block:: python

    INSTALLED_APPS = (
    ...
    'qa',
    'taggit',
    'hitcount',
    'django_markdown',
    ...
    )

Add the package urls to the project:

.. code-block:: python

    urlpatterns = [
        ...,
        url(r'^', include('qa.urls')),
        ...
    ]

Run migrations::

    python manage.py migrate

Once all the previous steps have been solved, check the settings topic to include those into your project settings file.

And that's it!

CAVEATS
-------
There is an issue with django-markdown-app versioning. It does not support django1.11(LTS) and 2 simultaneously.
If you have a project using django>=2.0, you will need to specify the django-markdown-app manually to the latest.
