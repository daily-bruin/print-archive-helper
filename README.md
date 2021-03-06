# print-archive-helper
This is an add-on to the main UCLA Print Archive project. Much of UCLA's news history is stored in large microfilm reels,
where the only way to accurately get the date for each page is to insert it into the database manually. The goal of this
helper site is to allow as many people as possible to contribute to the manual insertion of dates. 

GOALS:
The site will display a pdf page, the user will input the date he/she sees on the page, submit it, and it will be added to the database in real time. The site will keep showing images until the user clicks "I'm done!", or something along those lines. 

There should be a count that display how many pages are left! 

Getting Started:
Clone this directory.

Please download Python 3.5.1. Follow the instructions on this page if you need help. https://tutorial.djangogirls.org/en/python_installation/

Download PostgreSQL 9.5.4. If you have a Mac, you can use this, it's super easy :) http://postgresapp.com Once you have installed this, just click the elephant icon to start your server. 

Next, setup a virtual environment. Follow the instructions on this page if you need help. https://tutorial.djangogirls.org/en/django_installation/

Activate your virtual environment and then run "pip install -r requirements.txt". 

Open psql and run "CREATE DATABASE pdf_info"
Run "python manage.py makemigrations --settings=data_collection.data_app.local_settings" and
run "python manage.py migrate --settings=data_collection.data_app.local_settings"

To populate the database, run "python manage.py loaddata reel1.json --settings=data_collection.data_app.local_settings". 

In your terminal, navigate to the directory that has the "manage.py" file, then run "python manage.py runserver --settings=data_collection.data_app.local_settings". 

Navigate to localhost to see the site. 

To checkout the database on "localhost:8000/admin", you're going to need to create a superuser. To do this, type, "python manage.py createsuperuser --settings=data_collection.data_app.local_settings". It's going to ask you for a username and pw. 

After you've done that, navigate to localhost:8000/admin and click pdf to see the contents of the database.

Read through the Django Girls tutorial I linked to above to get familiar with Django if you have never used it before. 

