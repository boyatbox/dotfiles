Reload resource file and relaunch urxvt to see changes applied to .Xresource  
xrdb ~/.Xresources

###Powerline-shell:#  
https://github.com/powerline/fonts  

**Intsall powerline-shell:**  
sudo pip3 install powerline-shell  

**Generate config:**  

mkdir -p ~/.config/powerline-shell && \
powerline-shell --generate-config > ~/.config/powerline-shell/config.json

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


