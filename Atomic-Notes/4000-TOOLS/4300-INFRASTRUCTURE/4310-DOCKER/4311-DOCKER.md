Docker is used to run images, small versions of an operating software, or applications.


## Installing Docker
```bash
# Install docker 
sudo apt install docker.io -y
```

## Useful Commands
```bash
# List downloaded images
docker images

# Launching hello world test image
docker run hello-world

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
```