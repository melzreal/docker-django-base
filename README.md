## Base files for a docker-django application

Create a folder with your project name, cd into it and download this once inside it.
Then run the command to create your django project:

<pre><code>
docker-compose run web django-admin startproject whateverProjectName .
</code></pre>

Once that's created, edit the project's whateverProjectName/settings.py file and replace DATABASES with:

<pre><code>
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
  </code></pre>

run <pre><code>docker-compose up</code></pre> and you're good to go
