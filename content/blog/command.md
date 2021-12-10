---
title: "Command Bermanfaat"
date: 2021-12-10T07:01:57+07:00
draft: false
tags: [
    "command",
    "cli",
    "armbian"
]
---

Perintah-perintah bermanfaat untuk Ubuntu/Debian terutama handle STB:

```
Useful Linux commands for Ubuntu/Debian
---------------------------------------
Update/Install
--------------
sudo apt update                               Update repolists
sudo apt upgrade                              Upgrade system/programs
sudo apt autoremove                           Remove obsolete programs
sudo apt install programName                  Install program
sudo apt remove programName                   Remove program 
sudo aptitude install                         When having issue's with apt, aptitude can help to solve this
sudo apt update && sudo apt upgrade           Update and upgrade together/You can run multiple commands with &&
sudo dpkg -i packageName.deb                  Install .deb file

Root user
---------
sudo passwd                                   Change root password
su                                            Super User/Enter root user

Debug/Monitor
-------------
dmesg                                         Shows debug messages 
uname -a                                      Shows basic system information
env                                           Shows the environment information
htop                                          Hardware monitor

Switch terminal
---------------
ctrl + ALT + F4       (F1 - F6)                                    Open new terminal 4
ctrl + ALT + F1                                                    Go back to terminal 1
ctrl + ALT + F7                                                    Go back to desktop 

Reboot/Shutdown
---------------
sudo reboot                                   Reboot
sudo shutdown now                             Shutdown

CPU Tools
---------
cpufreq-set -g performance                    Set governor to performance
cpufreq-set -u 2Ghz                           Set max frequency for all cores
cpufreq-set -c 0-1 -u 1.8Ghz                  Set max frequency for specific cores
lscpu | grep MHz                              Show cpu frequency    
taskset -c 3 programName                      Use a specific core for an application   

Files/Directories
-----------------
nano /home/fileToRemove.txt                   Create a txt file with Nano. You could use any other texteditor.
touch filename                                Create an empty file, no matter what kind
cat /home/fileToRemove.txt                    Shows the content of a file
cp /home/fileToRemove.txt /home/copy.txt      Copy file
find /home/ -iname "*.txt"                    Search files that end with .txt
comm /home/fileToRemove.txt /home/copy.txt    Compare files
rm /home/fileToRemove.txt                     Remove file
mv /home/copy.txt ~/Documents/                Move file
mkdir /home/directoryToGoTo/                  Create directory
cd /home/directoryToGoTo/                     Go to directory
ls                                            List directory
ls -l                                         Gives more information about every file/directory
ls -l filename.txt                            Gives file information
pwd                                           Show current working directory
cd ..                                         Go to the above directory
rmdir /home/directoryToGoTo/                  Remove directory                             
wget http://www.website.com/file.txt          Download file

Zip/Tar/GunZip
--------------
zip myzip file1 file2 file3                   Create zip file
unzip myzip.zip                               Unzip file
tar xvf filename.tar
gunzip filename_tar.gz

Mount drives/USB Devices
------------
lsusb                                         List USB devices
lsblb                                         List attached drives
mount /mount/mountedDisk /dev/sda2            Mount drive
sudo chmod -R 777 /mount/mountedDisk          Give user read/write permissions
df -a                                         List all filesystems

Swap file/ZRam
--------------
sudo apt install zram-config                  Install zram script

sudo fallocate -l 8G /swapfile                Allocate 8GB for swapfile
sudo chmod 600 /swapfile                      Give the correct rights for the swapfile
sudo mkswap /swapfile                         Make it a swapfile
sudo swapon /swapfile                         Turn on the swapfile
sudo nano /etc/fstab                          Open fstab and add the line ...
  |_
       /swapfile swap swap defaults 0 0


Wifi
----
sudo nano /etc/network/interfaces 

and write:
 auto wlan0
 iface wlan0 inet dhcp 
                wpa-ssid {ssid}
                wpa-psk  {password}
				
				OR
				
nmcli device wifi rescan                                           Scan for available wifi networks
nmcli device wifi list                                             Show available wifi networks
nmcli device wifi connect SSID-Name password wireless-password	   Connect wifi

ip a                                                               Show ip
ifconfig                                                        
iwconfig

Change Keyboard Layout
----------------------
sudo dpkg-reconfigure keyboard-configuration                       Set keyboard layout

Add display resolution
----------------------
cvt 2560 1440 60                                                   Select the display resolution you want
# 2560x1440 59.96 Hz (CVT 3.69M9) hsync: 89.52 kHz; pclk: 312.25 MHz
Modeline "2560x1440_60.00"  312.25  2560 2752 3024 3488  1440 1443 1448 1493 -hsync +vsync

xrandr --newmode "2560x1440_60.00"  312.25  2560 2752 3024 3488  1440 1443 1448 1493 -hsync +vsync         Add resolution, everything after Modeline from cvt is copied after newmode

xrandr --addmode HDMI-1 2560x1440_60.00                                                                    Add the new resolution to your display

xrandr --newmode "2560x1440_60.00"  312.25  2560 2752 3024 3488  1440 1443 1448 1493 -hsync +vsync && xrandr --addmode HDMI-1 2560x1440_60.00 

Others
------
reset                                                              Clear terminal 
shift + page up                                                    Scroll up
shift + page down                                                  Scroll down 
tab                                                                Autocomplete
ctrl + c                                                           Quit for many programs 
date                                                               Show date/time
cal                                                                Show calender


Funny commands
--------------
sl                                                                 First need to install "sudo apt install sl", then try it out. It's great :) 
sl -alF
cmatrix
fortune/fortune-mod
cowsay 
figlet 
toilet 
ponysay 
inxi 
cat /dev/urandom 
:(){ :|:& };:                                                     Endless loop (useful to test CPU maximized temperatures)

Armbian
-------
sudo armbianmonitor -m                                             
sudo armbian-config

change cpu settings
sudo nano /etc/default/cpufrequtils
```

Tambahan pada `~/.bash_aliases`

```sh

############################
# my personal Aliases list #
############################
# to create the file  nano ~/.bash_aliases


# **** DIRECTORY LISTING in human-readable units ****
alias ll="ls -lhAF"
alias ..="cd .."
alias ...="cd ../../../"
alias back="cd $OLDPWD"

alias lsmount="mount |column -t"


# * Disk Space Usage in human-readable units,  including filesystem type *
alias dfh="df -Tha --total"

alias df="df -h --exclude=squashfs"


# * ALL files in a directory listed,  according their size *
alias du="du -ach | sort -h"


# * listing process table in detail *
alias psa="ps auxf"

alias dmesg="dmesg --human"


# * How to really CLEAR the terminal *
alias clr='printf "\033c"'

alias h="history"



# reload bash config
alias reload="source ~/.bashrc"

```

Sekarang bisa dieksekusi reloadnya dengan command:  `. ~/.bashrc` pada terminal

Ada spasinya yak, antara titik . dan ~/.bashrc