# Django Stars Backend Skeleton

Basic django template for project creation that don't need django to start a project.

## How to use

### Create new project

  1. Download and run the script:
  ```curl https://be.skeletons.djangostars.com/startproject | bash```
  2. Answer the questions.

### Create new application

Project created with *Django Stars Backend Skeleton* has overwritten `startapp` command that will create application with given name. Template will be chosen automatically based on your `settings.INSTALLED_APPS`.


## Template features

### Base teamplate

  * **Django** project formatted according to [Django Stars Code Style](https://codestyle.djangostars.com/) requirements
  * **django-environ** to keep all configuration in environment
  * **psycopg2** as default database driver
  * **django-extensions/ipython/ipdb** for debug purposes
  * **pytest** with **pylama** for testing
  * redefined **startapp** command to create app according to [Django Stars Code Style](https://codestyle.djangostars.com/) requirements

### Django REST Framework

add [DRF](http://django-rest-framework.org) to base template

### Celery

add [Celery](http://www.celeryproject.org/) to base template
