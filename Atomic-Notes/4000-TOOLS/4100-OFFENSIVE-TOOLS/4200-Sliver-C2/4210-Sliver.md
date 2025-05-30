## Installing Sliver
```bash
# Below is the easy way
wget https://github.com/BishopFox/sliver/releases/download/v1.5.43/sliver-client_linux
chmod 755 sliver-client-linux
mv sliver-client-linux /bin/sliver

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