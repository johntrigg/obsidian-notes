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

#
docker exec -it 74cc54e27dc4 sh
```