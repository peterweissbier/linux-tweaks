## faster compiling
1. use the command >>nproc<< to check your number of cpu threads
2. to be on the safe side use like 2-4 threads less for compiling
3. now edit your makepkg.conf
4. sudo nano /etc/makepkg.conf
5. edit it to the desired # of threads e.g.
        MAKEFLAGS="-j10(nproc)"

## manually import a specific recv key
gpg --recv-keys 893e8e9432898e

## [chaotix-aur for prebuilt packages](https://aur.chaotic.cx/)
What it is

Most packages available in this repo are automatically built from their respective AUR source package. However, there are a few exceptions, check out the packages repo to find out which ones.
The primary building cluster is a node in UFSCar's datacenter which is hosted in São Carlos, São Paulo, Brazil.

to install, follow the instructions on the website

## run doublecommander as root

uncheck "Allow only 1 copy of DC at a time" in Configuration >Options >Behavior

1. Open /usr/share/applications/doublecmd.desktop
2. Save as /usr/share/applications/root-doublecmd.desktop
3. Change the contents as follows:

Name=Double Commander Root

Exec=sudo doublecmd

sudo nano /etc/sudoers and add the following line

yourusername ALL = NOPASSWD: /usr/bin/doublecmd

add the created root-doublecmd.desktop to the desktop/taskbar to use it as a launcher
