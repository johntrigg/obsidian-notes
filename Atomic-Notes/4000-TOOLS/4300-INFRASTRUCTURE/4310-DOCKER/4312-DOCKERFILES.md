A dockerfile is often used with [[4311-DOCKER]] as a way to automate the building of images.

https://docs.docker.com/reference/dockerfile/

Below is an example of a dockerfile that would be used to create an Ubuntu image running an SSH server

```dockerfile
# FILENAME: Dockerfile 
FROM ubuntu:latest

# Set environment variable to avoid interactive prompts during package installation 
ENV DEBIAN_FRONTEND=noninteractive

# Install core utilities
RUN apt-get update && apt-get inst
```