# ansible-mac
Setup a new machine on Mac

`brew install --cask flameshot`
go to Finder > Applications and select the flameshot icon, and from menu bar choose open
go to settings "Private and secure" > scroll down to allow flameshot record screen


`brew install --cask raycast`
go to Finder > Applications and select the raycast icon, and from menu bar choose open

`brew install --cask nikitabobko/tap/aerospace`

install 1password for mac via browser https://1password.com/downloads/mac and unzip, run installer
in settings > developer > allow integration with 1password-cli
than run
`eval $(op signin)` 

run in terminal for gpg
```bash
GPG_TTY=$(tty)
export GPG_TTY
```

run ansible
```bash
ansible-playbook -bK local.yml
```
it will fail, because it cant login with 1password app in subprocess, but than run `chezmoi apply` from the terminal
close terminal


run wezterm from raycast
type `ezsh` - neovim should install all plugins

run ansible again

run stats for status bar from raycast launcher
run itsycal for status bar from raycast launcher

install nvm with script from https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating

Setup gGit

```bash
git config --global user.email "email"
git config --global user.name "name"
ssh-add --apple-use-keychain ~/.ssh/id_rklak
```
