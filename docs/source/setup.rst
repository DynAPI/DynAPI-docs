Setup
=====

.. _installation:

Installation
------------

To use DynAPI, first configure the system to your pleasing:

second, install the dependencies using pip:

.. code-block:: console

   (.venv) $ pip3 install -r requirements.txt

Configuration
----------------

configure the options given in 'api.conf.template' and save the file as 'api.conf'

Startup
----------------

start the server with the helper script 'dynapi' from root

.. code-block:: console

   (.venv) $ ./dynapi (this starts the flask api, and generates the swagger/redoc endpoint documentation dynamically for your DB)
