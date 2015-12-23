#Installation Instructions

*Make sure you have Python 2.7.6, virtualenv, pip and sqlite3/mysql installed*

1. Download or clone this repo.

2. Go to project home folder and run these commands:

    virtualenv venv 
    source venv/bin/activate 

3. This will create a virtual environment and activate it. 
   Now use pip to install dependencies with:

    pip install -r dev-requirements.txt

4. Now we have to prepare a database:

    python manage.py makemigrations (if any changes in model)
    python manage.py migrate --fake-initial

5. It will ask you to provide username, email and password. 

6. Run django server (dev only)
    python manage.py runserver 

7. Go to [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

8. Go to home page.

9. (note) Secret infomation such as SECRET_KEY is in sfvue/local_settings.py, 
   and this should not be committed. 
