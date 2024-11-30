Modified from this AUR package: [https://aur.archlinux.org/packages/initramfs-l14kbdlight/](https://aur.archlinux.org/packages/initramfs-l14kbdlight/)

This is a initcpio hook that can be used to turn the ASUS ux390 keyboard
backlight on during boot. This is usefull when prompted to type the LUKS
passphrase, for instance.

Build:

makepkg . 
sudo pacman -U ./initramfs-ux390ua-kb-*.pkg.tar.zst

Edit /etc/mkinitcpio.conf:

HOOKS=(base udev autodetect modconf block keyboard ux390ua_kb_backlight encrypt filesystems resume)

Regenerate initramfs:

sudo mkinitcpio -p linux

Reboot.
