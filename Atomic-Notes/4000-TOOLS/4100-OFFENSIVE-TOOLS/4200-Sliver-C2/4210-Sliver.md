## Installing Sliver
```bash
# Below is the easy way


wget -O /bin/sliver-server https://github.com/BishopFox/sliver/releases/download/v1.5.17/sliver-server_linux 
chmod 755 /bin/sliver-server

wget -O /bin/sliver https://github.com/BishopFox/sliver/releases/download/v1.5.17/sliver-client_linux 
chmod 755 /bin/sliver
# Below is the 'proper way'
# As root
curl https://sliver.sh/install | sudo bash

# Install c compiler for windows
sudo apt install mingw-w64

# Start the sliver service
systemctl enable sliver
systemctl start sliver
systemctl daemon-reload
```