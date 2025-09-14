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

$ vim /etc/apt/sources.list.d/ubuntu.sources

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

### Ubuntu Server

```
$ ip addr
$ cd /etc/netplan/
$ vim 50-cloud-init.yaml

[50-cloud-init.yaml]
network:
    version: 2
    ethernets:
        ens32:
            dhcp4: no
            addresses: [192.168.111.200/24]
            gateway4: 192.168.111.2
            nameservers:
                addresses: [192.168.111.2]

$ sudo su - root
$ passwd
$ reboot
$ ip addr
$ ping -c 3 google.com
$ ufw enable
$ apt -y install net-tools bzip2

// rust install
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
$ reboot
$ halt -p >> poweroff
```
