Assignment 2
# Reflection on Django Project Setup

During the setup of my Django project "my_project" with the "valera" app, I encountered several challenges that tested my troubleshooting skills. First, template inheritance didn't work initially because I forgot to create the `templates` directory inside the app and ensure `'APP_DIRS': True` in settings.py. The pages threw a TemplateDoesNotExist error. I solved this by double-checking the Django documentation and verifying file paths, then restarting the server.

Another issue was with URL configurations; the /about/ path wasn't resolving due to a missing include in the project-level urls.py. I debugged this by running `python manage.py check` and inspecting the traceback in the browser console, which pointed to the import error. Adding `path('', include('valera.urls'))` fixed it.

Git setup was tricky when pushing to GitHub, I got authentication errors due to 2FA. Generating a personal access token and using it instead of my password resolved this. Overall, these challenges reinforced the importance of reading error messages carefully and consulting official docs, making me more efficient for future projects.
