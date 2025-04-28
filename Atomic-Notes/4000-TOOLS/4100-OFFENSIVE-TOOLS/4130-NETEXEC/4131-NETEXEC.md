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
```
netexec smb target -u '' -p '' --shares  
netexec smb target -u username -p password --shares
```

## Resources
https://seriotonctf.github.io/2024/03/07/CrackMapExec-and-NetExec-Cheat-Sheet/