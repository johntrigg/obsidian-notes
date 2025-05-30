
```bash
# Install and configure
sudo apt update -y
sudo apt full-upgrade -y

# Install VS-Codium
wget -qO - https://gitlab.com/paulcarroty/vscodium-deb-rpm-repo/raw/master/pub.gpg \ 
| gpg --dearmor \ 
| sudo dd of=/usr/share/keyrings/vscodium-archive-keyring.gpg echo 'deb [ signed-by=/usr/share/keyrings/vscodium-archive-keyring.gpg ] https://download.vscodium.com/debs vscodium main' \ | sudo tee /etc/apt/sources.list.d/vscodium.list sudo apt update && sudo apt install codium

# Install system theme

# Make themes directory
mkdir -p ~/.themes

# Download the theme
wget https://github.com/johntrigg/triggonometry-kali-config/raw/refs/heads/main/rice/Sweet-Dark-v40.tar.xz

# Extract the theme (assuming it's a compressed archive)
tar -xvf Sweet-Dark-v40.tar.xz

# Move the theme to the appropriate directory
sudo mv Sweet-Dark-v40 /usr/share/themes

# Set the system theme manually

# Install icons

# Make icons directory
mkdir ~/.icons

# Download the icon theme
wget https://github.com/johntrigg/triggonometry-kali-config/raw/refs/heads/main/rice/candy-icons.tar.xz

# Extract the icon theme (assuming it's a compressed archive)
tar -xvf candy-icons.tar.xz

# Move the icon theme to the appropriate directory
cp -r candy-icons/ /usr/share/icons


# Make vpn directory

sudo mkdir -p /vpn && sudo chmod 777 /vpn

# Navigate to power manager > display > sleep never and switch off never

# Install core programs
sudo apt-get install tmux -y
sudo apt-get install golang -y
sudo apt-get install terminator -y
sudo apt-get install fastfetch -y

```

## oh-my-zsh
Run these one by one, manually, and not as root
```bash
# Install oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Install blokkzh prompt
curl -O https://raw.githubusercontent.com/KorvinSilver/blokkzh/master/blokkzh-downloader.zsh && zsh blokkzh-downloader.zsh $ZSH_CUSTOM && rm blokkzh-downloader.zsh
```
## .zshrc file
~/.zshrc
Paste to the bottom
```
if [ "$TMUX" = "" ]; then
    tmux
fi

# Created by `pipx` on 2024-03-09 07:10:56
export PATH="$PATH:/home/kali/.local/bin"
export JAVA_HOME="$JAVA_HOME"

fastfetch

```

## Configure Terminator
```bash
mkdir -p ~/.config/terminator

wget -O ~/.config/terminator/config https://raw.githubusercontent.com/johntrigg/triggonometry-kali-config/refs/heads/main/configurationFiles/terminatorConfig

# Modify font size as needed
```