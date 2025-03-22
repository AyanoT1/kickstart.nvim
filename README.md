# Ayano's neovim starter - kickstart.nvim configs

## Installation

### Windows (Powershell)

Start a Powershell as Admin and run:
```sh
winget install --accept-source-agreements chocolatey.chocolatey
```

```sh
choco install -y neovim git ripgrep wget fd unzip gzip mingw make
```

Reboot...

```sh
git clone https://github.com/AyanoT1/kickstart.nvim.git "${env:LOCALAPPDATA}\nvim"
```

```sh
nvim
```

### Debian

```sh
sudo apt update && sudo apt upgrade
```

```sh
sudo apt install make gcc ripgrep unzip git xclip curl

curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.tar.gz
sudo rm -rf /opt/nvim-linux-x86_64
sudo mkdir -p /opt/nvim-linux-x86_64
sudo chmod a+rX /opt/nvim-linux-x86_64
sudo tar -C /opt -xzf nvim-linux-x86_64.tar.gz

sudo ln -sf /opt/nvim-linux-x86_64/bin/nvim /usr/local/bin/
exec bash
```

```sh
git clone https://github.com/AyanoT1/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```

```sh
nvim
```

## Uninstallation

Windows:
```
rm "${env:LOCALAPPDATA}\nvim" -Force
```

Debian:
```
rm -rf "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```
