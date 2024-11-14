# **Python Command**

#### Mac Command

| Command                                              | Description                               |
| :--------------------------------------------------- | :---------------------------------------- |
| `pip install env`                                    | Install virtual environment               |
| `python3 -m venv env`                                | Create environment file for project       |
| `source env.bin/activate`                            | Active virtual environment                |
| `deactivate`                                         | deactivate environment                    |

#### Window Command

| Command                           | Description                       |
| --------------------------------  | ----------------------------------|
| `pip install venv`                | Install virtual environmen        |
| `pip freeze`                      | Check Status                      |
| `pip -m venv env`                 | Untracked files                   |
| `\env\Scripts\activate`           | File add to stage                 |
| `deactivate`                      | Modified files                    |
| `pip freeze > requirement.txt`    | Add all install package add into the requirement.txt                     |

#### Django Command

| Command                                                            | Description                                              |
| ------------------------------------------------------------------ | -------------------------------------------------------- |
| `django-admin startproject [name] .`                               | Create django project  |
| `django-admin startapp [name]`                                     | Create djagno app  |
| `python manage.py check`                                           | Checks the entire Django project for potential problems  |
| `python manage.py clearsessions`                                   | Expired sessions from the session storage   |
| `python manage.py makemessages -l languagecode`                    | Discovers translation strings and creates or updates translation files.   |
| `python manage.py compilemessages`                                 | Compiles the language translations from .po files to .mo files.   |
| `python manage.py createlanguage languagecode`                     | Creates a new language code for internationalization.  |
| `python manage.py createcachetable`                                | Creates the cache table in the database for caching.   |
| `python manage.py creategroup groupname`                           | Creates a new group for user permissions.   |
| `python manage.py dbshell`                                         | Launches the database command-line shell   |
| `python manage.py diffsettings`                                    | Displays differences between the project's settings and the default settings.   |
| `python manage.py dumpdata appname > data.json`                    | Creates a JSON or YAML dump of the database contents.   |
| `python manage.py flush`                                           | Clears the entire database and deletes all data.   |
| `python manage.py inspectdb > models.py`                           | Introspects the database and generates Django models based on existing tables.   |
| `python manage.py loaddata data.json`                              | Loads data from a JSON or YAML file into the database.   |
| `python manage.py sendtestemail`                                   | Sends a test email to verify email settings   |
| `python manage.py shell`                                           | Launches a Python interactive shell with Django initialized.   |
| `python manage.py showmigrations`                                  | Lists all applied and pending database migrations.   |
| `python manage.py sqlflush`                                        | Generates the SQL statements to flush the database.   |
| `python manage.py sqlmigrate appname migrationname`                | Displays the SQL statements for specific database migration.   |
| `python manage.py sqlsequencereset appname`                        | Generates the SQL statements to reset database sequences.   |
| `python manage.py squashmigrations appname`                        | Squashes existing database migrations into a single new migration.    |
| `python manage.py startapp appname`                                | Creates a new Django app within your project.   |
| `django-admin startproject projectname`                            | Creates a new Django project.  |
| `python manage.py test`                                            | Runs tests for all the test cases in your Django project.   |
| `python manage.py testserver`                                      | Runs a development server with the test database.   |
| `python manage.py collectstatic`                                   | Collects static files from all installed apps into a single directory.   |
| `python manage.py testserver`                                      | Runs a development server using the test database.   |
| `python manage.py runserver`                                       | Runserver your local server   |
| `python manage.py createsuperuser`                                 | Create superuser   |
| `python manage.py makemigrations`                                  | Create migrations   |
| `python manage.py migrate`                                         | Apply migration to database   |
| `python manage.py --help`                                          | Display a list of available commands  |
| `python manage.py migrate app_name zero`                           | Remove all migrations Zero   |

#### Case for python 

| Name                     | Case          |
| ------------------------ | ------------- |
| class                    | Camel_Case    |
| function                 | computer_fun  |
| package                  | all lower     |
| module                   | all lower     |
| variable                 | CamelCase     |
| Global                   | __Global__    |
| Instance Variable        |  Foo._Foo_a.  |
| constants                |  MAX_NUMBERS  |


#### Create a Virtual environment with different python version 

You should first ensure that Python is correctly installed and its 'Scripts' folder is in your PATH. 
Add path in system variable -
1. C:\Users\<YourUsername>\AppData\Local\Programs\Python\PythonXY
2. C:\Users\<YourUsername>\AppData\Local\Programs\Python\PythonXY\Scripts

| command                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------|
| C:\Users\\[YourUsername]>pip install venv                                                                               |
| D:\\[YourProject]>powershell                                                                                            |
| PS D:\[YourProject]> virtualenv -p C:\Users\\[YourUsername]\AppData\Local\Programs\Python\Python311\python.exe .venv    |


#### Add pylint 

| command                                         | Description                   |
| ------------------------------------------------| ----------------------------- |
| `python -m pip install pylint`                  | install pylint                |
| `pylint --generate-rcfile > pylintrc`           | generate a new pylintrc file  |
| `pylint myproject/`                             | run pylint for project        |
