Setup
=====

.. _installation:

Installation
------------

second, install the dependencies using pip:

.. code-block:: console

   (.venv) $ pip3 install -r requirements.txt

Configuration
----------------

To use DynAPI, first configure the system to your pleasing by configuring the options given in 'api.conf.template' and save the file as 'api.conf'

.. dropdown:: configuration file template:
   [api]
   # host:
   # where to host
   # recommended: 0.0.0.0, 127.0.0.1, localhost
   host=0.0.0.0
   
   # port:
   # which port to serve on
   # recommended: 3000, 5000, 5050, 8000, 8080
   port=8080
   
   # debug:
   # changes if server auto reloads, if debug tracebacks are shown in the browser and more
   debug=True
   
   # threaded:
   # changes if threading is activated or not (chose between threading or processes, dont activate both)
   threaded=True
   
   # processes:
   # changes how many processes run DynAPI (chose between threading or processes, dont activate both)
   processes=2
   
   [web]
   # redoc:
   # whether or not to provide the redoc documentation
   redoc=True
   
   # swagger:
   # whether or not to provide the swagger documentation
   swagger=True
   
   # docs:
   # bool for (read-the-docs) documentation
   docs=True
   
   #bools for allowing / disallowing CRUD methods
   [methods]
   get=True
   post=True
   put=True
   delete=True


[database]
# db_host:
# Host or IPv4 address of the database to connect to.
# Optional parameter.
# Default: localhost
db_host=<>

# db_port:
# Port of the database to connect to.
# Optional parameter.
# Default: 5432
db_port=<>

# db_user:
# User of the database to connect to.
db_user=<>

# db_password:
# Password of db_user with the database to connect to.
db_password=<>

# db_database:
# Database/Schema of the database to connect to.
db_database=<>

Startup
----------------

start the server with the helper script 'dynapi' from root

.. code-block:: console

   (.venv) $ ./dynapi (this starts the flask api, and generates the swagger/redoc endpoint documentation dynamically for your DB)
