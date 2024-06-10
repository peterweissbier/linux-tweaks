## pamac with flatpak & snap support

libpamac-full & dependencies
<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">https://aur.archlinux.org/packages/snapd</pre>
<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">https://aur.archlinux.org/packages/snapd-glib</pre>
<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">https://aur.archlinux.org/packages/libpamac-full</pre>

pamac-cli
<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">https://aur.archlinux.org/packages/pamac-cli</pre>

pamac-all
<pre style="margin-bottom: 0; border-bottom:none; padding-bottom:0.8em;">https://aur.archlinux.org/pamac-all.git</pre>

## remove password prompt from pacman, pamac, aliases or aur helpers (yay, paru)
1. sudo -i
2. sudo nano /etc/sudoers
3. at the bottom of the file add:
4. <your username> ALL=(ALL) NOPASSWD: ALL

## faster compiling
1. use the command >>nproc<< to check your number of cpu threads
2. to be on the safe side use like 2-4 threads less for compiling
3. now edit your makepkg.conf
4. sudo nano /etc/makepkg.conf
5. edit it to the desired # of threads e.g.
        MAKEFLAGS="-j10(nproc)"

## import any recv key
gpg --recv-keys 893e8e9432898e

## chaotix-aur for prebuilt packages
What it is

Most packages available in this repo are automatically built from their respective AUR source package. However, there are a few exceptions, check out the packages repo to find out which ones.
The primary building cluster is a node in UFSCar's datacenter which is hosted in São Carlos, São Paulo, Brazil.

to install, follow the instructions on https://aur.chaotic.cx/

## run doublecommander as root

uncheck "Allow only 1 copy of DC at a time" in Configuration >Options >Behavior

1. Open /usr/share/applications/doublecmd.desktop
2. Save as /usr/share/applications/root-doublecmd.desktop
3. Change the contents as follows:

[Desktop Entry]
Name=DoubleCmd Root
Comment=Double Commander is a cross platform open source file manager with two panels side by side.
Terminal=false
Icon=doublecmd
Exec=sudo doublecmd
Type=Application
Categories=Application;Utility;FileManager;

drag the new created root-doublecmd.desktop to the taskbar as a launcher
