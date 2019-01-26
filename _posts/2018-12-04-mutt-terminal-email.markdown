simple email client
```
$ sudo apt install mutt
```
configure
```
$ mkdir -p ~/.mutt/cache
$ touch ~/.mutt/muttrc
```
add the following lines to the file and then edit it "name, user and password"
```
set from = "user@gmail.com"
set realname = "Your Name"
set imap_user = "user@gmail.com"
set imap_pass = "password"
set folder = "imaps://imap.gmail.com:993"
set spoolfile = "+INBOX"
set postponed ="+[Gmail]/Drafts"
set header_cache =~/.mutt/cache/headers
set message_cachedir =~/.mutt/cache/bodies
set certificate_file =~/.mutt/certificates
set smtp_url = "smtp://user@smtp.gmail.com:587/"
set smtp_pass = "password"
set move = no 
set imap_keepalive = 900
```
```
$ nano ~/.mutt/muttrc
```
<a href="https://draculatheme.com/mutt/" target="_blank"><button class="button-download button-small pure-button">Download  dark theme</button></a>
```
$ mutt
```
<img src="https://skandyns.github.io/img/mutt.png"/>
