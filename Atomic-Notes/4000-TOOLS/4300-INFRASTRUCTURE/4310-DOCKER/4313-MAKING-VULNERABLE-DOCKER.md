Here, we'll make an intentionally vulnerable docker instance, for use teaching or in a CTF/King-of-the-Hill CTF environment.

Goal is to expose only one port (80), so we can use it for CTFD docker, have multiple vulnerabilities.

## Outline
- Port 80 Website:
    - king.txt hosted
    - command injection vulnerability
    - file upload vulnerability
    - lfi vulnerability
    - web console page for admin
    - sitemap.xml

- Privilege Escalation:
	- Writable /etc/passwd
	- SETUID binary
	- Root crontab running script

-Handling king.txt:
	- Should be relatively hidden
	- Should be served to the website
	- Should be a writable king.sh script somewhere that writes an im