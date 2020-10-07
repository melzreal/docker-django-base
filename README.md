## Base files for a docker-django application

Download the set, then do

__docker-compose run web django-admin startproject whateverProjectName .__

Then edit the project's composeexample/settings.py file and replace DATABASES with

  DATABASES = {
      'default': {
          'ENGINE': 'django.db.backends.postgresql',
          'NAME': 'postgres',
          'USER': 'postgres',
          'PASSWORD': 'postgres',
          'HOST': 'db',
          'PORT': 5432,
      }
  }

run docker compose up and you're good to go