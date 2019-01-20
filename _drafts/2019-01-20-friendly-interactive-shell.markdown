My favorite shell.

<img src="https://skandyns.github.io/img/fish-shell.png"/>

My simple prompt (fish_prompt.fish)
```
function fish_prompt
    set -l t ffffff
    set -l b 660066
    set -l a ffff00
    set_color $t -b $b
    echo -n " "(basename $PWD)" "
    set_color $a -b normal
    echo " ❯❯❯ "
end
```
```
sudo apt install fish
```
Switching to fish (default shell)
```
chsh -s /usr/bin/fish
```
Back to bash
```
chsh -s /bin/bash
```

