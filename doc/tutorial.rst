.. _demotutorial:

Demo Webapp Tutorial
====================

Getting started is pretty easy. The first thing to do is create a
configuration somewhere on your filesystem.  You'll need to add the correct
values for your configuration. When you're done the file should look something
like this::

    DEBUG = True
    SOURCE_DIR = '/path/to/rst/sources'
    BUILD_DIR = '/path/to/build/directory'
    DATABASE_URI = 'sqlite:////path/to/sqlite/db'
    SECRET_KEY = 'Your secret key'
    SEARCH = 'xapian'

Then you'll need to set an environment variable pointing to your configurate
file. On Linux you can set the environment variable with this command::

    $ export SPHINXWEB_SETTINGS=/path/to/your/configs/sphinxweb.cfg

Once this is done you're ready to build the documentation. Inside the
sphinx-demo-webapp directory execute this command::

    $ python build.py

This will build the documentation, and copy the static files from the build
directory to the webapp's static directory. You're then ready to start the
development server::

    $ python runserver.py

Now you can open up your browser and go to http://127.0.0.1:5000/
to view the documentation.
