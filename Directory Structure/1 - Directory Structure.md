## / - Root
### /home
##### - User home directories

Examples: 
``` sh
/home/littlesekii
/home/user
```
***
### /root
##### - Root home directory
***
### /bin
##### - Essential user command binaries

Examples: 
``` sh
ls
cp
mv
rm
cat
```

 You can see all paths containing binaries commands:
``` sh 
echo $PATH
```

To see from where a command come from:
``` sh 
which ls
which git
```
***
### /sbin
##### - System command binaries (administrative commands)

Examples:
``` sh
mount
fsck
reboot
```

You can see all paths containing binaries commands:
``` sh 
echo $PATH
```

To see from where a command come from:
``` sh 
which ls
which git
```
***
### /lib
##### - Essential shared libraries and kernel modules

Necessary libraries for boot, /bin, /sbin, etc;

Examples:
``` sh
/lib/x86_64-linux-gnu/
/lib/firmware/
```
***
### /etc
##### - Host-specific system configuration

Examples: 
``` sh
/etc/nginx/nginx.conf
/etc/ssh/sshd_config
/etc/hosts
```
***
### /usr
##### - Multiuser utilities and applications (secondary hierarchy)

Installed programs, libraries, documentation, etc;

Examples:
``` sh
/usr/bin
/usr/lib
/usr/share
```
***
### /mnt
##### - Mount point for a temporarily mounted filesystems

Manual mounting point;

Examples:
``` sh
/mnt/backup
```
***
### /media
##### - Mount point for removable media

Automatic mounting point;

Examples:
``` sh
/media/usb
/media/exthd
```
***
### /dev
##### - Device files

Linux treats hardware as files;

Examples:
``` sh
/dev/sda
/dev/null
/dev/tty
```
***
### /opt
##### - Add-on application software packages

Big programs, isolated, not coming from distro;

Examples:
``` sh
/opt/google/
/opt/idea/
/opt/sonarqube/
/opt/custom-app/
```

***
### /srv
##### - Data served by services

``` sh
/srv/www
/srv/ftp
/srv/git
```
***
### /var
##### - Variable files

Files that change over time;

Examples:
``` sh
/var/log
/var/lib
/var/cache
```

***
### /proc
##### - Virtual filesystem documenting kernel and process status as text files

Not real files;
Files created in memory;

Examples:
``` sh
/proc/cpuinfo
/proc/meminfo
```
***
### /boot
##### - Static boot loader files

Files used on boot;

Examples:
``` sh
/boot/vmlinuz     → kernel
/boot/initrd.img  → initramfs
/boot/grub/       → bootloader
```
***
### /tmp
##### - Temporary files

Any user can manage files here;
May be cleaned when system is rebooted;

Examples:
``` sh
/tmp/build123
```
***
### Summary

![[Pasted image 20260201212006.png]]
![[Pasted image 20260201213320.png]]