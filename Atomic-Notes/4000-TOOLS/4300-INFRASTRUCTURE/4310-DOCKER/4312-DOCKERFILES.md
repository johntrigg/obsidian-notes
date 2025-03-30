A dockerfile is often used with [[4311-DOCKER]] as a way to automate the building of images.

https://docs.docker.com/reference/dockerfile/

You might run a docker file with the below commands

```bash
# Use Dockerfile in current directory to make a docker instance called my-ubuntu-image
docker build -t my-ubuntu-image .
```
Below is an example of a dockerfile (filename: Dockerfile`)that would be used to create an Ubuntu image running an SSH server

```dockerfile
# FILENAME: Dockerfile 
FROM ubuntu:latest

# Set environment variable to avoid interactive prompts during package installation 
ENV DEBIAN_FRONTEND=noninteractive

# Install core utilities
RUN apt-get update 
RUN apt-get install -y  curl vim git iproute2 

# Install the openSSH server
RUN apt-get install -y openssh-server

# Create the necessary directory for the SSH daemon to run 
RUN mkdir /var/run/sshd

# Create a new user 'test' with password 'test' 
RUN useradd -m test && echo "test:test" | chpasswd 
# Ensure password authentication is enabled in SSH configuration 
RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication yes/' /etc/ssh/sshd_config && \ sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config 
# Expose port 22 for SSH connections 
EXPOSE 22 
# Start the SSH daemon in the background, then keep the container alive by tailing /dev/null 
CMD /bin/bash -c "/usr/sbin/sshd && tail -f /dev/null"
```