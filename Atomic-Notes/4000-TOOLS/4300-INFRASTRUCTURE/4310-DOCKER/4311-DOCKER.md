Docker is used to run images, small versions of an operating software, or applications. 

There are three core concepts:

- There are three core concepts:
    1. Docker Images - (Like ubuntu:latest), immutable blueprints or bases
    2. Docker Containers - Portable runtime instances of images used to run applications
    3. Docker Daemon - Service used to manage images and containers


## Installing Docker
```bash
# Install docker 
sudo apt install docker.io -y

# Install docker-compose
sudo apt install docker-compose -y
```

## Useful Commands
```bash
# List downloaded images
docker images

# Launching hello world test image
docker run hello-world

# Create a container called 'my-running-app' using the ubuntu-latest image, map container port 22 to host port 5000, and run the container in -d detached mode in the background
docker run -d -p 22:5000 --name my-running-app ubuntu:latest

# Check for images (running or not)
docker ps -a

# Get a shell on container id '74cc54e27dc4'
docker exec -it 74cc54e27dc4 sh

# Getting ubuntu docker
docker pull ubuntu

# launch it
docker run -it ubuntu bash

# Launch it and background it
docker run -it ubuntu bash &

# Kill running docker of name ubuntu-ssh
docker kill ubuntu-ssh

```