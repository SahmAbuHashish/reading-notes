# Reading Questions

### What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?

- Keep settings in environment variables.
- Write default values for production configuration (excluding secret keys and tokens).
- Don’t hardcode sensitive settings, and don’t put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.

---

### How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?

The WhiteNoise library contributes to the efficient serving of static files in a Django application by allowing for simplified and optimized serving of static assets directly from the application itself, without the need for a separate web server.

- Compression and Caching.
- Integration with Django.
- Simplicity and Ease of Use.

To integrate WhiteNoise into a Django project:

1. Install WhiteNoise: Install WhiteNoise

2. Configure Django Settings

   a. Add `'whitenoise.middleware.WhiteNoiseMiddleware'` to the `MIDDLEWARE` setting. Place it just after the `'django.middleware.security.SecurityMiddleware'` middleware.

   b. Add `'whitenoise.storage.CompressedManifestStaticFilesStorage'` to the `STATICFILES_STORAGE` setting. This enables WhiteNoise to serve static files and apply compression.

   c. Ensure that the `STATIC_ROOT` setting is defined and points to the directory where your static files will be collected.

3. Collect Static Files: Run the following command to collect your static files into the specified `STATIC_ROOT` directory:

4. Configure Web Server: If you're deploying your Django application using a separate web server, make sure to configure it to serve the static files directly from the `STATIC_ROOT` directory. 

---

### What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?

Cross-origin resource sharing (CORS) is a mechanism that allows restricted resources on a web page to be accessed from another domain outside the domain from which the first resource was served.

To implement and configure CORS in a Django project:

1. Install Django CORS Headers: Install the `django-cors-headers` package using pip:
```
$ pip install django-cors-headers
```

2. Configure Django Settings: Open your Django project's settings file (`settings.py`) and make the following changes:

   a. Add `'corsheaders'` to the `INSTALLED_APPS` setting.

   b. Add `'corsheaders.middleware.CorsMiddleware'` to the `MIDDLEWARE` setting. Place it as high as possible, just after `'django.middleware.security.SecurityMiddleware'`.

   c. Define the `CORS_ALLOWED_ORIGINS` setting to specify the list of allowed origins (domains) that are allowed to access your resources. For example:
   ```python
   CORS_ALLOWED_ORIGINS = [
       'http://example.com',
       'https://www.example.com',
   ]
   ```

   d. Optionally, configure other CORS settings such as `CORS_ALLOW_METHODS`, `CORS_ALLOW_HEADERS`, or `CORS_EXPOSE_HEADERS` based on your requirements.
