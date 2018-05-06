### Raspberry Pi

[Raspberry Pi](https://www.raspberrypi.org/)
username pi
passowrd: raspberry

wlan0: c8:e7:d8:ec:45:9c

eth0: b8:27:eb:0b:10:31


http://mirrors.ustc.edu.cn/help/raspbian.html


### 安装

	diskutil list
	diskutil unmountDisk /dev/disk<disk# from diskutil>
	sudo dd bs=1m if=image.img of=/dev/rdisk<disk# from diskutil> conv=sync
	
	
sudo raspi-config


**wifi**

https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md


**ssh**

https://www.raspberrypi.org/documentation/remote-access/ssh/unix.md
