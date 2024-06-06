## remove password prompt from pacman, pamac, aliases or aur helpers (yay, paru)
sudo -i
sudo nano /etc/sudoers
at the bottom of the file add:
<your username> ALL=(ALL) NOPASSWD: ALL

## faster compiling
lscpu
to check your number of cpu threads
sudo nano /etc/makepkg.conf
edit to
MAKEFLAGS="-j$(nproc)"

for weaker CPUs you can try and put a value that is half of the number of threads of your core, like for example
#MAKEFLAGS="-j6"

## import any recv key
gpg --recv-keys 893e8e9432898e

## chaotix-aur for prebuilt packages
What it is

Most packages available in this repo are automatically built from their respective AUR source package. However, there are a few exceptions, check out the packages repo to find out which ones.
The primary building cluster is a node in UFSCar's datacenter which is hosted in São Carlos, São Paulo, Brazil.

to install, follow the instructions on https://aur.chaotic.cx/

## crontab example 

@reboot ( sleep 90 ; sh /location/script.sh )
