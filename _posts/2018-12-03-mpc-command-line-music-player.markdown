enjoy the music on the command-line
```
$ sudo apt install mpd mpc
```
configure mpd
```
$ mkdir -p ~/.mpd/playlists
$ touch ~/.mpd/mpd.conf
```
mpd.conf (pulseaudio) - copy and paste
```
 bind_to_address "127.0.0.1"
 music_directory "~/Music"
 playlist_directory "~/.mpd/playlists"   
 db_file      "~/.mpd/mpd.db"  
 log_file      "~/.mpd/mpd.log"  
 pid_file      "~/.mpd/mpd.pid"  
 state_file     "~/.mpd/mpdstate"  
 audio_output {  

     type  "pulse"  
     name  "pulse audio"
     device         "pulse" 
     mixer_type      "hardware" 
 }  
 
 audio_output {
    type                    "fifo"
    name                    "my_fifo"
    path                    "/tmp/mpd.fifo"
    format                  "44100:16:2"
}
```
```
$ nano ~/.mpd/mpd.conf
```
disable automatic mpd startup at login (optional)
```
$ sudo systemctl disable mpd
$ sudo rm /etc/xdg/autostart/mpd.desktop
```
start
```
$ mpc
```
or (mpd disabled)
```
$ mpd
$ mpc
```
<img src="https://skandyns.github.io/img/mpc.png"/>

help my
```
$ mpc help
```
