We begin with our nmap scan of the beginning subnet.
```
sudo nmap -sC -sV -v -p- -o nmap 10.10.110.0/24 --min-rate 10000
```

We'll also run a few quick netexec checks.
```
# Guest Login
netexec smb 10.10.110.0/24 -u 'guest' -p ''

# Null Login
netexec smb 10.10.110.0/24 -u '' -p ''

# Local Authentication
netexec smb 10.10.110.0/24 -u '' -p '' --local-auth
```
