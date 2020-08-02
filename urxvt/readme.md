Reload resource file and relaunch urxvt to see changes applied to .Xresource  
xrdb ~/.Xresources

### Powerline-shell: #
https://github.com/powerline/fonts  

**Intsall powerline-shell:**  
sudo pip3 install powerline-shell  

**Generate config:**  
```
mkdir -p ~/.config/powerline-shell && \
powerline-shell --generate-config > ~/.config/powerline-shell/config.json
```
**Update .bashrc:**  

Append the folowing to .bashrc file


```
function _update_ps1() {
    PS1=$(powerline-shell $?)
}

if [[ $TERM != linux && ! $PROMPT_COMMAND =~ _update_ps1 ]]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

**Install Nerd Font - powerline glyph fix**
1. Download a Nerd font
https://github.com/ryanoasis/nerd-fonts#option-1-download-and-install-manually
2. Unzip and copy to ~/.fonts
3. Run the command fc-cache -fv to manually rebuild the font cache

