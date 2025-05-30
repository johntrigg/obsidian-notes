
```bash
# Install and configure
sudo apt update -y
sudo apt full-upgrade -y

# Install VS-Codium
wget -qO - https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/raw/master/pub.gpg \ 
| gpg --dearmor \ 
| sudo dd of=/usr/share/keyrings/vscodium-archive-keyring.gpg echo 'deb [ signed-by=/usr/share/keyrings/vscodium-archive-keyring.gpg ] https://download.vscodium.com/debs vscodium main' \ | sudo tee /etc/apt/sources.list.d/vscodium.list sudo apt update && sudo apt install codium

# Install system theme
#!/bin/zsh

# Make themes directory
mkdir -p ~/.themes

# Download the theme
wget https://github.com/johntrigg/triggonometry-kali-config/raw/refs/heads/main/rice/Sweet-Dark-v40.tar.xz

# Extract the theme (assuming it's a compressed archive)
tar -xvf Sweet-Dark-v40.tar.xz

# Move the theme to the appropriate directory
sudo mv Sweet-Dark-v40 /usr/share/themes

# Set the system theme
xfconf-query -c xsettings -p /Net/ThemeName -s "Sweet-Dark-v40"

# Make vpn directory

sudo mkdir -p /vpn && sudo chmod 777 /vpn

# Navigate to power manager > display > sleep never and switch off never

# Install core programs
sudo apt install tmux
sudo apt install golang -y

```
