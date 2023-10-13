## remove firefox as snap
[tutorial](https://www.youtube.com/watch?v=A7k5gQaOo9w)
```sh
sudo snap remove firefox sudo add-apt-repository ppa:mozillateam/ppa sudo nano /etc/apt/preferences.d/mozillateamppa 
```

Add the following lines and save using [Ctrl]+[X] 
```txt
Package: firefox* Pin: release o=LP-PPA-mozillateam Pin-Priority: 501 
```

```sh
sudo apt update 
sudo apt install firefox
```