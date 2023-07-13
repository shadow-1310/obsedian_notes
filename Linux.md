tags : #linux
## Add and Remove startup programme
### helpful links
- [see all programmes](https://www.maketecheasier.com/manage-startup-applications-ubuntu/)
- [see specific programme](https://www.makeuseof.com/manage-startup-applications-on-ubuntu/#:~:text=To%20add%20a%20new%20program,the%20Add%20Startup%20Program%20window.&text=Alternatively%2C%20you%20can%20click%20Browse,the%20program%3B%20although%20it's%20optional.)
### commands
- see list of startup programmes
```shell
systemd-analyze blame
```
- see if specific programme is on startup
```sh
systemctl list-unit-files | grep <program-name>
```
- disable the programme
```sh
sudo systemctl disable <program-name>
```
