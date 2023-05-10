# Arch Installation
## Arch Base Installation
* > timedatectl set-ntp true
    * set the system clock
* > timedatectl status
    * check the system clock
* > fdisk -l
    * list disk and partitions
* > cfdisk /dev/sda
    * select 'sda' as device to formatation and use
    * enter 'gpt' for UEFI systems
    * Partitions:
        * EFI     | 512MiB ~ 1GiB   | Efi System
        * Swap    | 2GiB ~ 4GiB     | Linux Swap  | Opcional
        * /       | 10GiB ~ 25GiB   | Linux Filesystem | generaly 1/4 of HDD
        * /Home   | 40GiB ~ 250GiB  | Linux Filesystem | all space left in HDD
    * White all changes and quit
* > mkfs.fat -F32 /dev/sda1
    * format and create the efi partitions
* > mkswap /dev/sda2
    * create swap file
* > swapon /dev/sda2
    * activate swap file
* > mkfs.ext4 /dev/sda3
    * format and create in format ext4 partiton /
* > mkfs.ext4 /dev/sda4
    * format and create in format ext4 partiton /home
* > mount /dev/sda3 /mnt
    * mount the / partition in /mnt
* > mkdir /mnt/home
    * create /home directory
* > mount /dev/sda4 /mnt/home
    * mount /home partition in /home directory
* > pacman -Sy vim
    * to install the text editor vim
* > vim /etc/pacman.conf
    * edit the pacman.conf file to enable multilib repository(used to run 32-bits software and libraries)
    * Uncomment the following lines:
        * [multilib]
        * Include = /etc/pacman.d/mirrorlist
* > pacstrap /mnt base base-devel linux linux-firmware
    * install essential packages
* > genfstab -U /mnt >> /mnt/etc/fstab
    * generate fstab
* > arch-chroot /mnt
    * change root into new system
* > ls /usr/share/zoneinfo/
    * to list the localization
* > ln -sf /usr/share/zoneinfo/America/Bahia /etc/localtime
    * substitui:
        * America = Country, find in /usr/share/zoneinfo, in this case 'America'
        * Bahia = Region, find in /usr/share/zoneinfo, in this case 'Bahia'
* > hwclock --systohc
    * set hardware clock
* > date
    * check time
* > vim /etc/locale.gen
    * uncomment the following line:
        * en_US.UTF-8 UTF-8
* > locale-gen
    * generate the locales
* > echo "LANG=en_US.UTF-8" > /etc/locale.conf
    * add locale to /etc file
* > echo "redfox" > /etc/hostname
    * create hostname 'redfox'
* > vim /etc/hosts
    * add the following lines:
        * 127.0.0.1 localhost
        * ::1   localhost
        * 127.0.1.1 redfox.localdomain  redfox
    * use tab after every block
* > passwd
    * root password
* > pacman -S grub efibootmgr os-prober
    * download grub
* > mkdir -p /boot/efi
    * creating boot directory
* > mount /dev/sda1 /boot/efi
    * mount efi partition in boot directory
* > grub-install --target=x86_64-efi --bootloader-id=GRUB --efi-directory=/boot/efi
    * install grub
* > grub-mkconfig -o /boot/grub/grub.cfg
    * generate grub configuration file
* > pacman -S dialog networkmanager network-manager-applet mesa mtools sudo
    * recommended packages
* > systemctl enable NetworkManager
    * enable service network manager
* > useradd -m -g users -G wheel redfox
    * adding user
* > echo "redfox ALL=(ALL) ALL" >>  /etc/sudoers
    * adding user to sudo list
* > passwd redfox
    * create password to user 
* > exit
    * exit the system
* > umount -R /mnt
    * Unmount the /mnt
* > reboot
    * reboot to new system

* login with the user account a.k.a redfox

> sudo pacman -S $GD
    * to install the corresponding graphic drivers
    * $GD = xf86-video-intel, to intel graphics
    * $GD = xf86-video-amdgpu, to amd graphics
    * $GD = nvidia nvidia-utils nvidia-setting, to nvidia graphics
    * $GD = xf86-video-ati, to ati graphics
> sudo systemctl enable fstrim.timer
    * if using ssd is recommended TRIM for better performance

# Arch Personalization
## Environment 
* I3
	> sudo pacman -Syu
		* update system to lastest packages
		
	> sudo pacman -S xorg-server xorg-xinit i3-wm --needed
		* install i3-wm (wich contain i3-gaps and a display manager)
		* install xorg 
		* install all dependences
* Gnome
    * > pacman -S gdm
    * > systemctl enable gdm
* KDE
    * > pacman -S sddm
    * > systemctl enable sddm
    * > pacman -S plasma konsole dolplin
* xfce
    * > pacman -S xfce4 xfce4-goodies xfce4-terminal
	
* login manager
    * > pacman -S slim xorg-server
    * > systemctl enable slim
## Customization and Apps
> sudo pacman -S noto-fonts ttf-ubuntu-font-family ttf-fira-code ttf-font-awesome -needed
	* install optional but recommended fonts
		
> sudo pacman -S alsa-utils alsa-plugins alsa-lib pavucontrol -needed
	* install sound drivers and tools
	
> sudo pacman -S dmenu w3m alacritty picom git neofetch htop wget polybar feh xclip neovim --needed
	* install additional tools:
		* browser: palemoon
		* status bar: polybar, to replace i3-bar
		* System Monitor: htop
		* wallpaper: feh
		* apps menu: dmenu
		* terminal emu.: alacritty
		* clipboard manager: xclip
		* text editor: neovim
		* terminal browser: w3m
		* compositor: picom

> sudo vim /etc/modprobe.d/alsa-base.conf
	* write the following
	* options snd_mia index=0
	* options snd_hda_intel index=1

> reboot
	* reboot the system
	
> cp /etc/X11/xinit/xinitrc ~/.xinitrc
	* copy the template xinit to home
	
> vim ~/.xinitrc
	* remove everything below '#start some nice programs'
	
> echo "exec i3" >> ~/.xinitrc
	* will write exec i3 on the .init file
	* to execute i3 every time the xsession is started
	
> w3m https://www.palemoon.org/download.shtml
	* access palemoon site and download palemoon gtk3 install
> sudo tar -xvf palemoon.tar.xz -C /opt/
	* extract the downloaded archive and move to /opt/
> sudo -sf /opt/palemoon/palemoon /usr/bin/palemoon
	* create a simbolic link in usr/bin from the executable
	
> startx
	* to start the X window session

## wallpaper
> mkdir ~/Images/wallpapers
	* rename you wallpaper image as linux_wallpaper.jpg and put it on ~/Images/wallpapers
> feh --bg-scale ~/Images/wallpapers/linux_wallpaper.jpg

## polybar
	
> mkdir ~/.config/polybar
> cp /etc/polybar/config.ini ~/.config/polybar/config.ini

> vim ~/.config/polybar/config.ini
	* comment the [module/wlan] section
*[module/pulseaudio]
*type = internal/alsa

## Installing SDL2
> sudo pacman -S sdl2 sdl2_mixer sdl2_image sdl2_ttf

## Customizing I3
* i3 config
set $mod mod4 (windows key)

* start a terminal
bindsym $mod+Return exec alacritty

* kill focused windows
bindsym $mod+q kill

* change focus
bindsym $mod+h focus left
bindsym $mod+j focus down
bindsym $mod+k focus up
bindsym $mod+l focus right

* move focused windows
* change focus
bindsym $mod+Shift+h focus left
bindsym $mod+Shift+j focus down
bindsym $mod+Shift+k focus up
bindsym $mod+Shift+l focus right

* comment lines:
	* bindsym $mod+h split h
	* bindsym $mod+v split v
	
	* bar {
	*		status_command i3bar
	* }

*# focus follows mouse yes|no 
focus_follows_mouse no

*# workspace auto back and forth yes|no 
workspace_auto_back_and_forth yes

*# i3 inner gaps
gaps inner 5

*# i3 outer gaps, e.g gaps outer|horizontal|vertical|top|left|bottom|right <gap_size>[px]
gaps top -10
gaps horizontal 2

*# i3 workspace specific gaps
workspace 2 gaps inner 2
workspace 2 gaps outer 0
workspace 2 gaps top -10

*# auto exec programs
exec_always --no-startup-id feh --bg-sscale ~/Images/wallpapers/linux_wallpaper.jpg
exec_always --no-startup-id killall -q polybar
exec_always --no-startup.id polybar meineBar
exec --no-startup-id picom -f --xrender -fence

## alacritty
> mkdir ~/.config/alacritty/alacritty.yml
> vim ~/.config/alacritty/alacritty.yml

## dotfile
all dot files must be pulled from git is easier

## zsh Terminal
* Go inside the oh my zsh site and copy the curl link the put on terminal