We begin with our nmap scan of the beginning subnet.
```
sudo nmap -sC -sV -v -p- -o nmap 10.10.110.0/24 --min-rate 10000
```