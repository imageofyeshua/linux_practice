// Shutdown
$ poweroff
$ shutdown -P now
$ halt -p
$ init 0

// Reboot
$ shutdown -r now
$ reboot
$ init 6

// Logout
$ logout
$ exit

// Virtual Console
Ctrl + Alt + F2 ~ F6 >> F2 is X Window Mode

$ chvt 3 >> change to 3 monitor
$ shutdown -h +5 >> poweroff after 5 minutes
$ shutdown -c >> poweroff cancel
$ shutdown -k +10 >> fake poweroff message

// Create several directories
$ mkdir -p abc/def/hij
$ cat <file> | less
$ file /dev/sda >> displays file detail

// Run level
0 : Power Off
1 : Rescue - System Recovery
2 : Multi-User - Not in use
3 : Multi-User - Text Mode
4 : Multi-User - Not in use
5 : Graphical - Graphic Mode
6 : Reboot

$ ls -l /lib/systemd/system/runlevel?.target
$ ls -l /lib/systemd/system/default.target
// default to multi-user : text-mode booting
$ ln -sf /lib/systemd/system/multi-user.target /lib/systemd/system/default.target
