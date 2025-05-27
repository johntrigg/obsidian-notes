
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
sudo -E ./mythic-cli
```
## References
https://redsiege.com/blog/2023/06/introduction-to-mythic-c2/
