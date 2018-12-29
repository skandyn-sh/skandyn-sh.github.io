step by step
```
$ sudo apt install mpd ncmpcpp
```
configure  mpd
```
$ mkdir -p ~/.mpd/playlists
$ touch ~/.mpd/mpd.conf
```
<a href="https://github.com/skandyn-sh/mpd/blob/master/mpd.conf" target="_blank">mpd.conf</a> (pulseaudio) - copy and paste to mpd.conf
```
$ nano ~/.mpd/mpd.conf
```
configure ncmpcpp
```
$ mkdir ~/.ncmpcpp
$ touch ~/.ncmpcpp/config
```
<a href="https://github.com/skandyn-sh/ncmpcpp/blob/master/config" target="_blank">config</a> - copy and paste to config

```
$ nano ~/.ncmpcpp/config
```
disable automatic mpd startup at login (optional)
```
$ sudo systemctl disable mpd
$ sudo rm /etc/xdg/autostart/mpd.desktop
```
start
```
$ ncmpcpp
```
or (mpd disabled)
```
$ mpd
$ ncmpcpp
```
key u - update database

<img src="https://skandyn-sh.github.io/img/ncmpcpp.png"/>

<a href="https://github.com/skandyn-sh/ncmpcpp/blob/master/ncmpcpp.png" target="_blank">that's my look ncmpcpp</a>

ncmpcpp useful keyboard keys
```
1 - playlist
2 - browse
3 - search engine
4 - media library
5 - playlist editor
6 - tag editor
7 - outputs
8 - music visualizer
p - play/pause
s - stop
c - clear playlist
q - quit
> - next song
< - previous track
\ - classic and alternative view
l - song lyrics for current song
= - clock
+ - increase volume 2%
- - decrease volume 2%
```
