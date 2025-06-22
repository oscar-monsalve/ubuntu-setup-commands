# After-installation Ubuntu commands

1. Essentials:

```shell
sudo apt-get update && sudo apt-get upgrade
```

```shell
sudo apt-get update && sudo apt-get upgrade
```

```shell
sudo apt-get install build-essential
```

```shell
sudo apt install curl
```

```shell
sudo apt install git
```

zsh shell and oh-my-zsh:
```shell
sudo apt install zsh
```

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

```shell
sudo apt install fd-find
```

```shell
sudo apt install ripgrep
```

python3-venv is required for python in neovim:
```shell
sudo apt install python3-venv
```

sudo apt instal xclip

sudo apt install btop

4. Install python libs:
    - sudo apt install python3-pip (optional)
    - sudo apt install python3-numpy
    - sudo apt install python3-matplotlib
    - sudo apt install python3-scienceplots

    If there are problems using pip3 installing a python package like: "error: externally-managed-environment",
    use pipx instead:

    ```
    sudo apt install pipx
    ```

    ```
    pipx install <package-name>
    ```

5. Steps to change the default max-line-length for the python lsp sever:
    - Create the file `pycodestyle` in the directory `~/.config/pycodestyle`
    - In `pycodestyle`, write:
    ```python
    [pycodestyle]
    max-line-length = 110
    ```



## Install neovim (Ubuntu)
```shell
sudo apt install neovim
```

Vimtex.nvim installation:
```shell
- sudo apt-get update && sudo apt-get install latexmk xdotool biber okular
```


## Install AnyDesk (Ubuntu)

1. Download the .deb file from the AnyDesk webpage.
2. Using the terminal, in the directory of the .deb file, paste:
```
sudo apt --fix-broken install /home/om/Downloads/anydesk/anydesk_6.3.1-1_amd64.deb
```
NOTE: check for the latest .deb package.

## Solve the hour difference netween Windows and Ubuntu (Dual-boot)
https://www.youtube.com/watch?v=lA3kNvI6WGU


## Firefox config

### Open tab in background

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

### Avoid opening a bookmark closes its menu or folder

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
