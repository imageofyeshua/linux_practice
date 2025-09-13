## After Installing

// root login setting

```
// root user password setting
$ sudo su - root
$ passwd

// system setting >> user >> enable auto login
### Ubuntu Budgie
$ vim /etc/lightdm/lightdm.conf

    [SeatDefaults]
    autologin-user=root
    autologin-user-timeout=0

$ vim /etc/apt/sources/list.d/ubuntu.sources

    [Erase: noble-updates noble-backports]

$ apt update

[Settings >> Network]

    ipv4: address: 192.168.111.100 netmask: 255.255.255.0 gateway: 192.168.111.2 dns: 192.168.111.2

$ reboot
$ ip addr
$ apt -y install net-tools gedit bzip2

// firewall
$ ufw enable
```
