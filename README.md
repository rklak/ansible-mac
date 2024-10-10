# ansible-mac
Setup a new machine on Mac

## Disable Natural scrolling
Open Settings > Trackpad > Scroll & Zoom

## Vivaldi browser
Download vivaldi from https://vivaldi.com/pl/download/

## Install Homebrew
Run: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

## Install Git
Run: `brew install git` 

## Install ansible
Run: `brew install ansible`

## Install Cask apps

### Flameshot
`brew install --cask flameshot`
go to Finder > Applications and select the flameshot icon, and from menu bar choose open
go to settings "Private and secure" > scroll down to allow flameshot record screen


### Raycast
`brew install --cask raycast`
go to Finder > Applications and open the raycast icon

### Aerospace
`brew install --cask nikitabobko/tap/aerospace`
go to Finder > Applications and open the aerospace icon

## Install 1password
install 1password for mac via browser https://1password.com/downloads/mac and unzip, run installer
in settings > developer > allow integration with 1password-cli
than run: `eval $(op signin)` 

## Prepare GPG
Run: 
```bash
GPG_TTY=$(tty)
export GPG_TTY
```
## Run ansible
```bash
ansible-playbook -bK local.yml
```
it will fail, because it cant login with 1password app in subprocess, but than run `chezmoi apply` from the terminal and it will try to login with 1password app correctly
*close terminal*

## Configure whats left

* run wezterm from raycast
* type `ezsh` - neovim should install all plugins
* run ansible again
* run stats for status bar from raycast launcher
* run itsycal for status bar from raycast launcher
* install nvm with script from https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating

## Setup Git

```bash
git config --global user.email "email"
git config --global user.name "name"
ssh-add --apple-use-keychain ~/.ssh/id_rklak
```
## Done
