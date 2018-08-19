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

See more in: [Dockerfile](Dockerfile)

## Compose file

This Compose file defines two services, web and redis.

### Web service

* Uses an image that’s built from the Dockerfile
in the current directory.

* Forwards the exposed port 5000 on the container to
port 5000 on the host machine. We use the default port
for the Flask web server, 5000.

### Redis service

It uses a public Redis image pulled from the Docker Hub registry.

See in: [docker-compose.yml](docker-compose.yml)