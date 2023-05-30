# Django-demo-project

A step-by-step demo from the [official tutorial website](https://docs.djangoproject.com/en/4.2/intro/).

## Content

- [Writing your first Django app, part 1](https://docs.djangoproject.com/en/4.2/intro/tutorial01/)
  - `django-admin startproject mysite`
  - `python manage.py runserver`
  - `python manage.py startapp polls`
  - You should always use **`include()`** when you include other URL patterns. **`admin.site.urls`** is the only exception to this.
  - We changed `polls/views.py`, `polls/urls.py` and `mysite/urls.py` in Part 1.

- [Writing your first Django app, part 2](https://docs.djangoproject.com/en/4.2/intro/tutorial02/)
  - `python manage.py migrate`
  - The migrate command looks at the INSTALLED_APPS setting and creates any necessary database tables according to the database settings in your mysite/settings.py file and the database migrations shipped with the app (we’ll cover those later). You’ll see a message for each migration it applies.
  - Like we said above, the default applications are included for the common case, but not everybody needs them. If you don’t need any or all of them, feel free to comment-out or delete the appropriate line(s) from INSTALLED_APPS before running migrate. The migrate command will only run migrations for apps in INSTALLED_APPS.
  - `python manage.py makemigrations polls`
  - By running makemigrations, you’re telling Django that you’ve made some changes to your models (in this case, you’ve made new ones) and that you’d like the changes to be stored as a migration.
  - `python manage.py sqlmigrate polls 0001` (check SQL only)
  - The sqlmigrate command doesn’t actually run the migration on your database - instead, it prints it to the screen so that you can see what SQL Django thinks is required. It’s useful for checking what Django is going to do or if you have database administrators who require SQL scripts for changes.
  - `python manage.py migrate`
  - The migrate command takes all the migrations that haven’t been applied (Django tracks which ones are applied using a special table in your database called django_migrations) and runs them against your database - essentially, synchronizing the changes you made to your models with the schema in the database.
  - Remember the three-step guide to making model changes:
    - Change your models (in models.py). 
    - Run `python manage.py makemigrations` to create migrations for those changes 
    - Run `python manage.py migrate` to apply those changes to the database.
  - `python manage.py createsuperuser`
  - Generating admin sites for your staff or clients to add, change, and delete content is tedious work that doesn’t require much creativity. For that reason, Django entirely automates creation of admin interfaces for models.
  - `python manage.py runserver`
  - We changed polls/models.py, polls/admin.py and mysite/settings.py to migrate and manage databases and create admin site in Part 2.

- [Writing your first Django app, part 3](https://docs.djangoproject.com/en/4.2/intro/tutorial03/)
- The render() function takes the request object as its first argument, a template name as its second argument and a dictionary as its optional third argument. It returns an HttpResponse object of the given template rendered with the given context.
- The get_object_or_404() function takes a Django model as its first argument and an arbitrary number of keyword arguments, which it passes to the get() function of the model’s manager. It raises Http404 if the object doesn’t exist.
- There’s also a get_list_or_404() function, which works just as get_object_or_404() – except using filter() instead of get(). It raises Http404 if the list is empty.
- We wrote new views. 

- [Writing your first Django app, part 4](https://docs.djangoproject.com/en/4.2/intro/tutorial04/)
- 
- [Writing your first Django app, part 5](https://docs.djangoproject.com/en/4.2/intro/tutorial05/)
- 
- [Writing your first Django app, part 6](https://docs.djangoproject.com/en/4.2/intro/tutorial06/)
- 
- [Writing your first Django app, part 7](https://docs.djangoproject.com/en/4.2/intro/tutorial07/)
- 
- [Writing your first Django app, part 8](https://docs.djangoproject.com/en/4.2/intro/tutorial08/)
- 
- [Advanced tutorial: How to write reusable apps](https://docs.djangoproject.com/en/4.2/intro/reusable-apps/#advanced-tutorial-how-to-write-reusable-apps)
- 
- [What to read next](https://docs.djangoproject.com/en/4.2/intro/whatsnext/)
- 
- [Writing your first patch for Django](https://docs.djangoproject.com/en/4.2/intro/contributing/)
- 