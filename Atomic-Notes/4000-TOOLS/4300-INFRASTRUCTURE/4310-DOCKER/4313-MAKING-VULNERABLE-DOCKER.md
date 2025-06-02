Here, we'll make an intentionally vulnerable docker instance, for use teaching or in a CTF/King-of-the-Hill CTF environment.

Goal is to expose only one port (80), so we can use it for CTFD docker, have multiple vulnerabilities.

## Outline
- Port 80 Website:
    - king.txt hosted
    - command injection vulnerability
    - file upload vulnerability
    - lfi vulnerability (have valuable file in html comments?)
    - web console page for admin
    - sitemap.xml

- Privilege Escalation:
	- Writable /etc/passwd
	- SETUID binary
	- Root crontab running script

-Handling king.txt:
	- Should be relatively hidden
	- Should be served to the website
	- Should be a writable king.sh script somewhere that writes an almost immutable king.txt file

- -Rules
	- Nothing destructive
	- Do not try to make it to root user, goal is to make it to admin user who can write a bash script that controls king.txt


## Running
Vulnerable site hosted at 
https://github.com/johntrigg/vuln-site

```bash
# Clone the site and cd in
git clone https://github.com/johntrigg/vuln-site.git
cd vuln-site

# Build and run the container
docker build -t vuln-site .

# Run the vuln-site container, map host port 8080 to container 80
docker run -d -p 8080:80 --name vuln-site-container vuln-site

# Check that it's running
docker ps


```

### Files
The dockerfile
```dockerfile
FROM php:8.2-apache

# Install dependencies and prepare environment
RUN apt-get update && \
    apt-get install -y procps && \
    docker-php-ext-install pdo pdo_mysql && \
    mkdir -p /var/www/html/uploads && \
    chmod 777 /var/www/html/uploads

# Copy all web files into the container
COPY www/ /var/www/html/

# Expose port 80 (Apache default)
EXPOSE 80


