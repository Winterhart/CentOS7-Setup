# Install GUI Environment from Minimal Setup

Look at all available group list

     yum group list

Install GNOME Desktop and UI Tool

    yum groupinstall "GNOME Desktop" "Graphical Administration Tools"

Install other GUI package

    yum groupinstall "Server with GUI"

Setup GNOME as default loader

    ln -sf /lib/systemd/system/runlevel5.target /etc/systemd/system/default.target

Restart the computer

    reboot

Tutorial from: https://www.itzgeek.com/how-tos/linux/centos-how-tos/install-gnome-gui-on-centos-7-rhel-7.html

## (Optional) Update your built with root
Login as root

    su

Enter your password

    ******************
launch yum update

    yum update

## (Optional) Take a look at Yum cheat sheet


Cheat sheet: https://access.redhat.com/sites/default/files/attachments/rh_yum_cheatsheet_1214_jcs_print-1.pdf

