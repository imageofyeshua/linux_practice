## Ubuntu Server

```
$ sudo apt install net-tools
$ sudo apt install openssh-server
$ sudo systemctl status ssh
$ sudo systemctl start ssh
$ sudo ufw allow ssh
$ sudo ufw enable
$ sudo ufw status
```

## connection from Windows

```
$ ssh -l kainos <ip-addr>
```

## Rocky Linux Setting

```
$ gsettings set org.gnome.software download-updates false
$ systemctl disable dnf-makecache.service
$ systemctl disable dnf-makecache.timer

$ cd /etc/yum.repos.d/
$ mkdir backup
$ mv *.repo backup

$ vim This.repo
```

### This.repo >> copy & paste

[baseos]
name=Rocky Linux $releasever - BaseOS
baseurl=https://dl.rockylinux.org/vault/rocky/9.6/BaseOS/x86_64/os/
gpgcheck=0

[appstream]
name=Rocky Linux $releasever - AppStream
baseurl=https://dl.rockylinux.org/vault/rocky/9.6/AppStream/x86_64/os/
gpgcheck=0

[extras]
name= Rocky Linux $releasever - Extras
baseurl=https://dl.rockylinux.org/vault/rocky/9.6/extras/x86_64/os/
gpgcheck=0

[plus]
name= Rocky Linux $releasever - Plus
baseurl=https://dl.rockylinux.org/vault/rocky/9.6/plus/x86_64/os/
gpgcheck=0

[crb]
name=Rocky Linux $releasever - CRB
baseurl=https://dl.rockylinux.org/vault/rocky/9.6/CRB/x86_64/os/
gpgcheck=0

```
$ dnf clean all

$ cd /etc/NetworkManager/system-connections/
$ ls <check connection network: ensXXX.nmconnection>
```

[ensXXX.nmconnection]

[ipv4] method=manual
address1=192.168.111.100/24,192.168.111.2
dns=192.168.111.2

```
$ cd
$ nmcli connection down ensXXX
$ nmcli connection up ensXXX

$ reboot
$ ifconfig ensXXX

// turn-off selinux
$ sestatus
$ grubby --update-kernel ALL --args selinux=0
$ reboot
$ sestatus

$ dnf -y install firewall-config

// resolution change
$ vim /etc/default/grub
>> GRUB_CMDLINE_LINUX="... selinux=0 vga=773"

// apply setting
$ grub2-mkconfig -o /boot/grub2/grub.cfg
$ reboot

```
