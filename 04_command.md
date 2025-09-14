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
