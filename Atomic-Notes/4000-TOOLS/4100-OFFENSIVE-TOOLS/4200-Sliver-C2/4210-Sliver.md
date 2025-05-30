## Installing Sliver
```bash
# Below is the easy way
wget -O /bin/sliver-server https://github.com/BishopFox/sliver/releases/download/v1.5.17/sliver-server_linux 
chmod 755 /bin/sliver-server

wget -O /bin/sliver https://github.com/BishopFox/sliver/releases/download/v1.5.17/sliver-client_linux 
chmod 755 /bin/sliver

# Unpack assets, as user
sliver-server unpack --force

# Windows C Compiler
sudo apt install mingw-w64



```
We can make it run on startup by making a service
```bash
vi /etc/systemd/system/sliver.service
# Paste below file
```

```
[Unit]
Description=Sliver
After=network.target
StartLimitIntervalSec=0

[Service]
Type=simple
Restart=on-failure
RestartSec=3
User=root
ExecStart=/bin/sliver-server daemon

[Install]
WantedBy=multi-user.target
```
Then
```bash
chmod 600 /etc/systemd/system/sliver.service
systemctl enable sliver && systemctl start sliver

# If you run into errors, it might be because sliver files already exist on your system, in /home/kali/.sliver, /root/.sliver, and ~/.sliver

# Check that the server is up
netstat -antopul


```

## Adding a New Operator
```bash
cd ~
sliver-server
# Review command
[server] sliver > help new-operator
[server] sliver > new-operator -n attacker -l tun0

[server] sliver > new-operator -n attacker2 -l 0.0.0.0
[server] sliver > multiplayer

# New session
# Import the attacker config
sliver import attacker_0.0.0.0.cfg


```

## Armory
Sliver's armory is a plugin 
```bash

```

## HackTheBox Cheatsheet
