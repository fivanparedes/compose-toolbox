# Compose toolbox

## Python everywhere runner

This is a small helper that creates a container with all the Python deps you have declared in your `requirements.txt` file and then run it, passing to the compose any argument you would pass to a python command.

In my work, I have another project that runs on Flask (which is all containerized), and separately I have a batch tool also written in Python. Since I need the script to communicate with the containerized API, I made this compose to be able to communicate with Flask's Docker network.

### Usage

Modify the `requirements.txt` to your needs and then just run:

`docker-compose run --rm python [args]`

If you need this container to communicate with any other Docker container out there, just uncomment the `external_default` network (and rename it as you need).