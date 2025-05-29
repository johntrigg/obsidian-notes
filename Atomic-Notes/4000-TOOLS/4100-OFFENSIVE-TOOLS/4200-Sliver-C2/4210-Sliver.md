## Installing Sliver
```bash
# As root
curl https://sliver.sh/install | sudo bash

# Install c compiler for windows
sudo apt install mingw-w64

# Start the sliver service
systemctl enable sliver
systemctl start sliver
systemctl daemon-reload
```