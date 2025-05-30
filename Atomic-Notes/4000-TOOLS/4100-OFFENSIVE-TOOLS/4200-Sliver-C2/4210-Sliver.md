## Installing Sliver
```bash
# Below is the easy way
wget -O /bin/sliver-server https://github.com/BishopFox/sliver/releases/download/v1.5.17/sliver-server_linux 
chmod 755 /bin/sliver-server

wget -O /bin/sliver https://github.com/BishopFox/sliver/releases/download/v1.5.17/sliver-client_linux 
chmod 755 /bin/sliver

# Unpack assets
sliver-server unpack --force

# Windows C Compiler
sudo apt install mingw-w64



```
We can make it run on startup by making a service
