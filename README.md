# After-installation Ubuntu commands

1. sudo apt update
2. sudo apt upgrade
3. sudo apt-get install build-essential

4. To install a package from python:
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
    The number after "=" sets the maximum length of a line in python to trigger the warning.

Install curl:
sudo apt install curl

Install git:
sudo apt install git

Install neofetch:
sudo apt install neofetch

Install htop:
sudo apt install htop

Install zsh shell and oh-my-zsh:
- sudo apt install zsh
- sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Install ripgrep:
sudo apt install ripgrep

Install python virtual environment (requierement for python in nvim):
sudo apt install python3-venv

Vimtex installation (Optional):
- sudo apt-get update
- sudo apt-get install latexmk
- sudo apt-get install xdotool
- sudo apt-get install biber
- sudo apt install zathura
- sudo apt install okular

## Install neovim (Ubuntu)
```
sudo apt install neovim
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
