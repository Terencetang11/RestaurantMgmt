# Restaurant Management Web App
 	By: Terence Tang
 	tangte@oregonstate.edu
 	CS 340 Databases
 	12/5/2020

## Included files:
    - app
        - webapp.py
        - db_credentials.py (log-in credentials for mariaDB)
        - static (bootstrap and images)
        - templates (html and js scripts)
        - db_connector (fx for making queries to mariaDB)
    - docs -> project documentation
    - lib -> sql queries
    - requirements.txt

## Description:
    Web-based restaurant management app implemented with Python3 with MariaDB SQL backend.  Allows restauranteurs the ability to track their ingredient stock, manage their menu items, pricing and scheduling of chefs and specialty dining items.  Showcases relationship management of entity types across ingredients, menu items, cuisine types, and chefs via a web-based front-end for ease of use.

    Additionally supplied is the project documentation which provides a project and database outline, Entity Relationship (ER) Diagram, DB Schema, and detailed description of the web app's functionality with regards to CRUD operations.


## Environment Requirements:
    - project implemented with Python3 and Flask framework
    - backend implemented with mysql (which needs to be installed)
    - backend utilizes MariaDB, which you will need to have set up and available for this project
    - bash shell required
    - virtualenv module installed

## Installation
### Set-up Virtual Environment
    Console instuctions to set up virtual environment (venv) for web app:
    - virtualenv venv -p $(which python3) 
    - source ./venv/bin/activate
    - pip3 install --upgrade pip
    - pip install -r requirements.txt

### Set-up Database Credentials for MariaDB
    Update the db_credentials.py file with your access credentials to your MariaDB instance:
    ```python
    host = 'your_host_name'
    user = 'your_user_name'
    passwd = 'your_password'
    db = 'your_db_name'
    ```
### Deploy Flask app on your local machine
    Console instuctions to run the Restaurant Mgmt flask app.  This will host the webapp on your local machine at port :8080
    ```bash
    source ./venv/bin/activate
    export FLASK_APP=./app/webapp.py
    python -m flask run -h 0.0.0.0 -p 8080 --reload
    ```