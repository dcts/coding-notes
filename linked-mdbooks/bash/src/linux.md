# LINUX Basics

In Linux, everything is a file.

## UBUNTU Shortcuts

```bash
SHIFT + ALT + T              # opens Terminal
CTRL + ALT + SHIFT + K       # computer shutdown (custom shortcut)
```

## UBUNTU Folderstructure

- **/bin** binaries
  * executable files (you can call them from terminal)
  * binary (ready to run, not readable for humans)
  * essential (a lot of system needed programs)
- **/boot** boot files
  * linux kernel (**/boot/vmlinuz**)
  * initial RAM disk image
  * boot loader (GRUB -> **/boot/grub/grub.conf**)
- **/dev** device nodes
  * all devices represented here as files
  * **/dev/sda1** (sda -> name of disk)
  * usb devices / cpu / etc...
- **/etc** configuration files
  * system-wide configuration files
  * some shell scripts
  * all files are human readable
- **/home** users folders
  * each user has its own user-folder here
  * private data, pictures, videos etc...
- **/lib** libraries
  * libraries required by the programs in **/bin** folder
  * (library is a set of functions that are shared between programs)
- **/lost+found** recovered files
  * only exists when using ext4 file system (most linux distros use it)
  * recovery folder used by the ext4 file system
  * seperate folder for every ext4 partition
  * empty unless something happens (used for recovery)
- **/media** automatic mount point
  * automatic mounting of removable media such as USB drives, CD-ROM etc.
  * when properly setup usb drives should appear here!
  * mounting = accessing
- **/mnt** manual mount point
  * similar to **/media** folder, but its usually used for manual mounting
- **/opt** optional software
  * not essential
  * often used to install commercial programs (dropbox etc.)
- **/proc** kernel files
  * virtual file-system for the linux kernel
  * not touched by a user
- **/root** root home
  * do not mix with /
  * the same as your user home directory but its for the root account!
- **/run** early temp
  * recently introduced
  * tempoirary file-system
  * used early in system boot (before other temp folder become availible!)
- **/sbin** system binaries
  * binaries
  * essential
  * run by the super user
- **/srv** service data
  * service files installed on your system
  * for example a http webserver
- **/tmp** temporary files
  * temporary files
  * this directory is usually cleaned on reboot
- **/usr** user binaries
  * the largest folder after **/home**
  * contains all programs used by a regular user (thousands of programs)
  * **/usr/bin** binaries of programs installed by your distro
  * **/usr/lib** libraries used by the binaries
  * **/usr/share/doc** documentation files for programs installed on system
- **/var** variable files
  * files that change all the time
  * **/var/log** stores log files (that monitors processes)
