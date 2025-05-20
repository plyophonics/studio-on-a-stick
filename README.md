# Studio On A Stick

Studio On A Stick is a project to help you create a bootable USB stick / laptop
running Ubuntu Studio with a curated list of software.

Everything you need is documented in this README.

## Initial Install

To begin with, download and install Ubuntu Studio on either a laptop, or a USB
stick using the instructions here: https://ubuntustudio.org/download/

## Post Install Updates

```bash
sudo apt update
sudo apt full-upgrade
sudo snap refresh
```

## Install Essential Software from Offical Repositories

```bash
sudo apt install \
    build-essential \
    fail2ban \
    mosh \
    zsh \
    byobu \
    vim \
    neovim \
    python3-neovim
```

## Install Signal Messenger

Instructions sourced from https://signal.org/download/

```bash
# NOTE: These instructions only work for 64-bit Debian-based
# Linux distributions such as Ubuntu, Mint etc.

# 1. Install our official public software signing key:
wget -O- https://updates.signal.org/desktop/apt/keys.asc | gpg --dearmor > signal-desktop-keyring.gpg;
cat signal-desktop-keyring.gpg | sudo tee /usr/share/keyrings/signal-desktop-keyring.gpg > /dev/null

# 2. Add our repository to your list of repositories:
echo 'deb [arch=amd64 signed-by=/usr/share/keyrings/signal-desktop-keyring.gpg] https://updates.signal.org/desktop/apt xenial main' |\
  sudo tee /etc/apt/sources.list.d/signal-xenial.list

# 3. Update your package database and install Signal:
sudo apt update && sudo apt install signal-desktop
```

## Install Element Messenger

Instructions sourced from https://element.io/download

```bash
sudo apt install -y wget apt-transport-https
‍
sudo wget -O /usr/share/keyrings/element-io-archive-keyring.gpg https://packages.element.io/debian/element-io-archive-keyring.gpg
‍
echo "deb [signed-by=/usr/share/keyrings/element-io-archive-keyring.gpg] https://packages.element.io/debian/ default main" | sudo tee /etc/apt/sources.list.d/element-io.list

sudo apt update

sudo apt install element-desktop
```

## Install OBS Studio

Instructions sourced from https://obsproject.com/download/

```bash
sudo add-apt-repository ppa:obsproject/obs-studio
sudo apt update
sudo apt install obs-studio
```

## Install Brave Browser

Instructions sourced from https://brave.com/linux/

```bash
sudo apt install curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser
```

## Install Google Chrome

* Download link https://www.google.com/chrome/what-you-make-of-it/
* Verify keys https://www.google.com/linuxrepositories/

## Install ProtonVPN

* On Ubuntu https://protonvpn.com/support/official-linux-vpn-ubuntu
* On Chrome / Brave https://protonvpn.com/download-chrome-extension
* On Firefox https://protonvpn.com/support/official-linux-vpn-ubuntu

## Resources

### Understanding 7-band EQs with the 7 Bad System Dwarves

[7 Bad System Dwarves](https://www.rationalacoustics.com/pages/the-7-bad-system-dwarves)
represent frequency bands you'd typically encounter when making / mixing music.

They're also what most 7-band EQs (eg: BOSS GE7) would typically help control.