# Post-installation Ubuntu commands

### Essentials:

```shell
sudo apt-get update && sudo apt-get upgrade
```

```shell
sudo apt update && sudo apt upgrade
```

```shell
sudo apt-get install build-essential
```

```shell
sudo apt install curl git fd-find ripgrep python3-venv xclip btop
```


### zsh shell and oh-my-zsh. Logout to set changes

```shell
sudo apt install zsh
```

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

```shell
chsh -s $(which zsh)
```

```shell
echo $SHELL
```

### Ghostty

[Ghostty terminal](https://ghostty.org/download)


### Install neovim (Ubuntu)

lua 5.1.5:
```shell
curl -L -R -O https://www.lua.org/ftp/lua-5.1.5.tar.gz
```

```shell
tar zxf lua-5.4.8.tar.gz
```

```shell
cd lua-5.1.5.tar.gz
```

```shell
make all test
```

luarocks 3.11.1
```shell
wget https://luarocks.org/releases/luarocks-3.11.1.tar.gz
```

```shell
tar zxpf luarocks-3.11.1.tar.gz
```

```shell
cd luarocks-3.11.1
```

```shell
./configure && make && sudo make install
```

```shell
sudo luarocks install luasocket
```

```shell
lua
```

```shell
require "socket"
```

neovim:
```shell
curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.tar.gz
sudo rm -rf /opt/nvim
sudo tar -C /opt -xzf nvim-linux-x86_64.tar.gz
```

Vimtex.nvim installation:
```shell
- sudo apt-get update && sudo apt-get install latexmk xdotool biber okular
```


### fzf

```shell
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```


### Python

Python-lsp-sever change default max-line-length:
Create the file `pycodestyle` in the directory `~/.config/pycodestyle`. In `pycodestyle`, write:

```python
[pycodestyle]
ignore = E302
max-line-length = 110
```

Install python libs:

```shell
sudo apt install python3-numpy
```

```shell
sudo apt install python3-matplotlib
```

```shell
sudo apt install python3-pytest
```

```shell
sudo apt install python3-scienceplots
```

```shell
sudo apt install python3-prettytable
```

```shell
sudo apt install python3-pip
```

If there are problems using pip3 installing a python package like: "error: externally-managed-environment",
use pipx instead:

```shell
sudo apt install pipx
```

```shell
pipx install <package-name>
```

Python generate lib requirements.txt:
```shell
pipx install pipreqs
```


### Albert spotlight-like finder

```shell
echo 'deb http://download.opensuse.org/repositories/home:/manuelschneid3r/xUbuntu_24.10/ /' | sudo tee /etc/apt/sources.list.d/home:manuelschneid3r.list
curl -fsSL https://download.opensuse.org/repositories/home:manuelschneid3r/xUbuntu_24.10/Release.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/home_manuelschneid3r.gpg > /dev/null
sudo apt update
sudo apt install albert
```


### Inkscape

```shell
sudo add-apt-repository universe
sudo add-apt-repository ppa:inkscape.dev/stable
sudo apt-get update
sudo apt install inkscape
```


### Spotify

```shell
curl -sS https://download.spotify.com/debian/pubkey_C85668DF69375001.gpg | sudo gpg --dearmor --yes -o /etc/apt/trusted.gpg.d/spotify.gpg
echo "deb https://repository.spotify.com stable non-free" | sudo tee /etc/apt/sources.list.d/spotify.list
sudo apt-get update && sudo apt-get install spotify-client
```


### Gimp

```shell
sudo apt install gimp
```


### Arduino-cli

[arduino_language_server.lua](https://github.com/neovim/nvim-lspconfig/blob/master/lsp/arduino_language_server.lua)

[arduino-cli installation](https://arduino.github.io/arduino-cli/1.2/installation/)

[arduino-language-server](https://github.com/arduino/arduino-language-server)


### AnyDesk (Ubuntu)

1. Download the .deb file from the AnyDesk webpage.
2. Using the terminal, in the directory of the .deb file, paste:
```
sudo apt --fix-broken install /home/om/Downloads/anydesk/anydesk_6.3.1-1_amd64.deb
```
NOTE: check for the latest .deb package.


### Solve the hour difference netween Windows and Ubuntu (Dual-boot)
https://www.youtube.com/watch?v=lA3kNvI6WGU


### Firefox config

#### Open tab in background

1. Open Firefox
2. In the search bar, type and accept the dialog:
```
about:config
```
3. Search:
```
browser.tabs.loadBookmarksInBackground
```
4. If the configuration is set to *false*, change it to *true*.

#### Avoid opening a bookmark closes its menu or folder

To avoid the bookmark's menus to close when opening a bookmark, do:

1. Open Firefox
2. In the search bar, type and accept the dialog:
```
about:config
```
3. Search:
```
browser.bookmarks.openInTabClosesMenu
```
4. If the configuration is set to *true*, change it to *false*.
