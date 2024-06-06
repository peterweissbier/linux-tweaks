## remove password prompt from pacman, pamac, aliases or aur helpers (yay, paru)
1) sudo -i
2) sudo nano /etc/sudoers
at the bottom of the file add:
<your username> ALL=(ALL) NOPASSWD: ALL
