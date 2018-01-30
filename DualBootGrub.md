
# Dual Boot Installation with Grub
Installation of Grub2 and dual boot with windows 10

If your Grub configuration is not as you like follow this tutorial.
First reinstall Grub.

    sudo yum reinstall grub2-tools

Login as root in a terminal

    su
In another terminal , get information about your Windows 10 hard drive, in my case it was named '/dev/sdb1'

    sudo fdisk -l

In my configuration, my windows 10 disk was on another hard drive. **Follow only if you are in the same situation.**

In the root terminal, navigate to the grub configuration directory

     cd  /etc/grub.d/



Now we must find the UUID of your Windows 10 hard drive, enter this command in your non-root terminal

    ls -l /dev/disk/by-uuid

Find the UUID code next to your disk something like: 40S863A9D8619F12

Now in the root terminal enter the command:

    nano 40_custom

Inside this file enter your windows 10 configuration using GRUB standard. Use the UUID code previously found inside the configuration. In my case my config is:

    menuentry 'Windows 10' {
            insmod ntfs
            insmod ntldr
            insmod part_msdos
            insmod search_fs_uuid
            search --fs-uuid --no-floppy --set=root 40S863A9D8619F12
            ntldr /bootmgr
    }

Save and exit nano. Now we need to generate a new GRUB configuration file. Enter the command:

    grub2-mkconfig --output=/boot/grub2/grub.cfg

Voilà !!!! Try the configuration with a fresh restart

Source:
http://dareneiri.github.io/Configuring-Grub-2-on-CentOS-7/
https://ihaveabackup.net/article/grub2-entry-for-windows-10-uefi


## (Optional) Install GRUB customizer

If you want to have a sexy GRUB menu you can install grub-customizer using this tutorial:
https://centos.pkgs.org/7/epel-x86_64/grub-customizer-5.0.6-1.el7.x86_64.rpm.html







