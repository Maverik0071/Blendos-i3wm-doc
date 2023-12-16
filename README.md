# Blendos-i3wm-doc
Understanding the Blendos Yaml config

Download Archlinux or Endeavour OS and out it on a usb

after get the archlinux and log into it, make sure that you do not have an operationg system and just make sure that it goes into Xorg after you boot back into it. 
After that is done:

type in sudo pacman /etc/pacman.conf and put in:

" [breakfast]
 SigLevel = Never
 Server = https://pkg-repo.blendos.co "

then open up a terminal and put in:

"sudo pacman -Sy akshara"

then type in the terminal:

"sudo pacman -S mkinicpio"

then in the terminal type in:

"/etc/mkinitcpio.conf" and go all the way down to "HOOKS" and put in:

"akshara".  Then exit out of that then go to your text editor and and go in "/system" directory and type in the text editor

"/system.yaml" then input this 

"copy and paste this below or type this out"

# if you have to type this out then it should take like 5 minutes

# /system.yaml

repo: 'https://pkg-repo.blendos.co/'

impl: 'https://github.com/blend-os/tracks/raw/main'

track: 'xfce4'

packages:
    - 'micro' # the best text editor out there ;)
    - 'firefox'
    - 'caddy'
    - 'networkmanager'

services:
    - 'caddy'
    - 'NetworkManager"

package-repos:
    - name: 'chaotic-aur'
      repo-url: 'https://cdn-mirror.chaotic.cx/$repo/$arch'

then go back to the terminal and type:

" sudo akshara update "

# if you ever have to update and it doesnt work then you have go back to the "system.yaml" file and then check the packages.  Then it should work.

After thats done, just "git clone" my file and compy and paste tose and that should work.  Change the package if you like but theres hyprland and i3 window manager and it does work.  
