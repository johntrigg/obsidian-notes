Netexec is a powerful tool often used for exploitation in Active Directory Environments, though it can broadly be used against most windows targets.

## Testing Authentication

```
# Guest Login
netexec smb target -u 'guest' -p ''

# Null Login
netexec smb target -u '' -p ''

# Local Authentication
netexec smb target -u username -p password --local-auth
```
## Resources