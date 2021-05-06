Sources:
--------  
https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-app-using-gunicorn-to-app-platform
https://medium.com/trabe/deploying-a-flask-application-with-gunicorn-and-docker-2bc7c4c10dd4


configuration  
-------------

[comment]: <> (config.py: application configuration  )

Application Factory
-------------------

[comment]: <> (app/__init__.py: application package constructor  )

Blueprints
----------

[comment]: <> (app/main/__init__.py: main blueprint creation  )

[comment]: <> (app/main/views.py: routes of the application)

[comment]: <> (app/main/errors.py: error handlers  )

[comment]: <> (**the modules are imported at the bottom of the app/main/__init__.py script to avoid errors due to circular dependencies**  )

[comment]: <> (The blueprint is registered with the application inside the create_app&#40;&#41; factory function  )

[comment]: <> (app/__init__.py: main blueprint registration  )

[comment]: <> (app/main/errors.py: error handlers in main blueprint)

[comment]: <> (the form objects are also stored inside the blueprint in the app/main/forms.py module.  )

Application Script
------------------
osteotomy.py: main script  
The configuration is taken from the environment variable FLASK_CONFIG if it’s defined, or else the default configuration is used  
Linux:
export FLASK_APP=osteotomy.py
Windows:
set FLASK_APP=osteotomy.py

Unit Tests
----------

[comment]: <> (tests/test_basics.py: unit tests  )

flask test


Database Setup
--------------

[comment]: <> (&#40;venv&#41; $ flask db upgrade  )


flask Shell
-----------
flask shell

Running the Application
-----------------------
(venv) $ flask run  
