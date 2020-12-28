# capstone_ai_enterprise_wf_app_naveen
Python based Flask webapp (e2e AI Enterprise workflow)
Usage notes
===============

All commands are from this project directory.


To test app.py
---------------------

.. code-block:: bash

    ~$ python app.py

or to start the flask app in debug mode

.. code-block:: bash

    ~$ python app.py -d

Go to http://0.0.0.0:8080/ and you will see a basic website that can be customtized for a project.
    

To build the docker container
--------------------------------

.. code-block:: bash

    ~$ docker build -t capstone-ai-wf-flask-app .

Check that the image is there.

.. code-block:: bash

    ~$ docker image ls
    
You may notice images that you no longer use. You may delete them with

.. code-block:: bash

    ~$ docker image rm IMAGE_ID_OR_NAME

And every once and a while if you want clean up you can

.. code-block:: bash

    ~$ docker system prune


Run the unittests
-------------------

Before running the unit tests launch the `app.py`.

To run only the api tests

.. code-block:: bash

    ~$ python unittests/ApiTests.py

To run only the model tests

.. code-block:: bash

    ~$ python unittests/ModelTests.py


To run all of the tests

.. code-block:: bash

    ~$ python run-tests.py

Run the container to test that it is working
----------------------------------------------    

.. code-block:: bash

    ~$ docker run -p 4000:8080 capstone-ai-wf-flask-app

Go to http://0.0.0.0:4000/ and you will see a basic website that can be customtized for a project.



