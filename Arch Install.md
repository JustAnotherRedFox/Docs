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
* > pacman -S vim
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
* > pacman -S dialog htop networkmanager network-manager-applet mesa mtools sudo
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

* > sudo pacman -S $GD
    * to install the corresponding graphic drivers
    * $GD = xf86-video-intel, to intel graphics
    * $GD = xf86-video-amdgpu, to amd graphics
    * $GD = nvidia nvidia-utils nvidia-setting, to nvidia graphics
    * $GD = xf86-video-ati, to ati graphics
* > sudo systemctl enable fstrim.timer
    * if using ssd is recommended TRIM for better performance
## Arch Base Dualboot
* > timedatectl set-ntp true
* > fdisk -l
    * select 'sda' as device to formatation and use
    * enter 'gpt' for UEFI systems
    * Partitions:
        * Swap    | 2GiB ~ 4GiB     | Linux Swap  | Opcional
        * /       | 10GiB ~ 25GiB   | Linux Filesystem | generaly 1/4 of HDD
        * /Home   | 40GiB ~ 250GiB  | Linux Filesystem | all space left in HDD
    * White all changes and quit
* > mkswap /dev/sda5
* > swapon /dev/sda5
* > mkfs.ext4 /dev/sda6
    * make file system '/' in format ext4
* > mkfs.ext4 /dev/sda7
    * make file system '/home' in format ext4
* > mount /dev/sda6 /mnt
* > mkdir /mnt/home
* > mount /dev/sda7 /mnt/home
* > pacstrap /mnt base linux linux-firmware vim ntfs-3g base-devel
* > mkdir /mnt/mnt/win
* > mount /dev/sda4 /mnt/mnt/win
    * mount windows primary partition(c:) in /mnt/mnt/win
* > genfstab -U /mnt >> /mmnt/etc/fstab
* > arch-chroot /mnt
* > ln -sf /usr/share/zoneinfo/America/Bahia /etc/localtime
* > hwclock --systohc --utc
* > vim /etc/locale.gen
    * uncomment line: pt_BR.UTF-8 UTF-8
* > locale-gen
* > echo "LANG=pt_BR.UTF-8" > /etc/locale.conf
* > echo "redfox" >> /etc/hostname
* > vim /etc/hosts
    * add the following lines:
        * 127.0.0.1 localhost
        * ::1   localhost
        * 127.0.1.1 redfox.localdomain  redfox
    * use tab after every block
* > mkinitcpio -p
* > passwd
    * root password
* > pacman -S grub efibootmgr dosfstools os-prober mtools networkmanager
* > mkdir /boot/EFI
* > mount /dev/sda2 /boot/EFI
	* mount the EFI system
* > grub-install --target=x86_64-efi --bootloader-id=grub_uefi --recheck
* > grub-mkconfig -o /boot/grub/grub.cfg

* if windows is not located, type:
	> echo "GRUB_DISABLE_OS_PROBER=false" >> /boot/grub/grub.cfg
    > grub-mkconfig -o /boot/grub/grub.cfg
* > systemctl enable NetworkManager
* > useradd -m  wheel redfox
* > passwd redfox
    * user password
* > pacman -S sudo 
* > echo "redfox ALL=(ALL) ALL" >> /etc/sudoers
* > exit
    * exit the system
* > umount -R /mnt
    * Unmount the /mnt
* > reboot
    * reboot to new system

* login with the user account a.k.a redfox

* > sudo pacman -S $GD
    * to install the corresponding graphic drivers
    * $GD = xf86-video-intel, to intel graphics
    * $GD = xf86-video-amdgpu, to amd graphics
    * $GD = nvidia nvidia-utils nvidia-setting, to nvidia graphics
    * $GD = xf86-video-ati, to ati graphics
* > sudo systemctl enable fstrim.timer
    * if using ssd is recommended TRIM for better performance

# Arch Personalization
## Environment 
* I3
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
## Applications