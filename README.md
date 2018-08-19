# Compose Test 

## app.py

redis is the hostname of the redis container on the
application's network using its default port (6379)

See in: [app.py](app.py)

**Requirements:** in [requirements.txt](requirements.txt)

## Dockerfile

It builds a Docker image that contains all the
dependencies the Python application requires, including
Python itself.

* Build an image starting with the Python 3.4 image.

* Add the current directory . into the path /code
in the image.

* Set the working directory to /code.

* Install the Python dependencies.

* Set the default command for the container to
python app.py.