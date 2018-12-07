Creating and activating a swap file (path: /swapfile), then adding it to /etc/fstab

For an example of a 1GB swap file (1M * 1024)
```
sudo dd if=/dev/zero of=/swapfile bs=1M count=1024
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile   
sudo sh -c 'echo "/swapfile swap swap defaults 0 0" >> /etc/fstab'
```
You can check if it works
```
free -m
```
clean swap
```
sudo swapoff -a
```
```
sudo swapon -a
```
