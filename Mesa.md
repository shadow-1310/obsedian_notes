## update to latest release
- https://itsfoss.com/install-mesa-ubuntu/#:~:text=What%20is%20Mesa%3F,Intel%20and%20AMD%20graphics%20hardware.

#### get information about graphics card
```sh
sudo lshw -C display
```
or
```sh
hwinfo --gfxcard --short
```
- [blog](https://www.cyberciti.biz/faq/ubuntu-linux-install-nvidia-driver-latest-proprietary-driver/)
install nvidia driver
```sh
sudo apt install nvidia-driver-535 nvidia-dkms-535
```