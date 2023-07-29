# Arch Linux

Arch Linux *mkinitcpio* hook for remote unlock of an encrypted root device via SSH.

```
$ mkinitcpio --hookhelp ssh-encrypt
==> Help for hook 'ssh-encrypt':
Enable remote unlock of an encrypted root device via SSH

Usage:

ssh unlock@<host>

Installation:

1. Copy authorized SSH keys to /etc/dropbear/authorized_keys
2. Replace hook 'encrypt' with 'ssh-encrypt' in /etc/mkinitcpio.conf
3. Add required kernel parameters
4. Rebuild initramfs

Device configuration kernel parameter:

cryptdevice=<device>:<name>[:<options>]

cryptdevice=/dev/disk/by-label/label:example
cryptdevice=UUID=62fce35d-8941-490a-9fd3-9c21c946bce5:ab3aa190-3534-4a05-8fc5-09c53cdd4c87:allow-discards,debug

Network configuration kernel parameter:

ip=<address>::<gateway>:<subnet>::<interface>:<method>

ip=::::::dhcp
ip=172.16.0.2::172.16.0.1:255.255.255.0:::off

==> This hook has runtime scripts:
  -> pre-mount hook
```

See https://wiki.archlinux.org/title/makepkg#Usage for installation.
