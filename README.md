
# Bash script to enable ec module.
## You use this script at your own risk.
I took commands from https://www.reddit.com/r/Fedora/comments/mbzj8h/ec_sys_module/
##  Required packages 
```
dnf install rpmdevtools
```
```
dnf install yum-utils
```
##  Additional info
* If doesn't work you can try disable secure boot in BIOS.
* You can add ec_sys.write_support=1 in /etc/default/grub.
* Also I added script to disable fan on MSI GS66 12UGH or you can use https://github.com/dmitry-s93/MControlCenter

##  Usefull comends
### Enable ec_sys module:
```
sudo modprobe ec_sys write_support=1
```
### Localization of ec file
```
/sys/kernel/debug/ec/ec0/io
```
## It has tested on Fedora 36, 37, 38, 39 for kernel:
* kernel-5.17.1-300.fc36.src.rpm
* kernel-5.17.2-300.fc36.src.rpm
* kernel-5.17.3-300.fc36.src.rpm
* kernel-5.17.3-302.fc36.src.rpm
  * Note: for this kernel I used parameter ./script https://fedora.cu.be/linux/development/36/Everything/source/tree/Packages/k/kernel-5.17.3-302.fc36.src.rpm - for more detail please read commit log
* 5.17.5-300.fc36.src.rpm
  * Note: example ./script https://fedora.cu.be/linux/development/36/Everything/source/tree/Packages/k/kernel-5.17.5-300.fc36.src.rpm - if You have a question, please ask it
* 5.17.6-300.fc36.x86_64.src.rpm
* 5.17.7-300.fc36.x86_64.src.rpm
* 5.17.8-300.fc36.x86_64.src.rpm
* 5.17.9-300.fc36.x86_64.src.rpm
* 5.17.10-300.fc36.x86_64.src.rpm - ?
* 5.17.11-300.fc36.x86_64.src.rpm
* 5.17.12-300.fc36.x86_64.src.rpm
* 5.17.13-300.fc36.x86_64.src.rpm
* 5.17.14-300.fc36.x86_64.src.rpm
* 5.18.5-200.fc36.x86_64.src.rpm
* 6.6.2-201.fc39.src.rpm
### Feel free to modify, change, distributed this script
