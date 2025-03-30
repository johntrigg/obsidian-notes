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




### Files
The dockerfile
```dockerfile
FROM php:8.2-apache

RUN apt-get update && \
    apt-get install -y procps && \
    docker-php-ext-install pdo pdo_mysql && \
    mkdir /var/www/html/uploads && \
    chmod 777 /var/www/html/uploads

COPY www/ /var/www/html/

EXPOSE 80

```