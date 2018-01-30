
# Installation of Spotify

Install the COPR plugin and EPEL

    $ sudo yum install yum-plugin-copr epel-release

Enable this repo

    $ sudo yum copr enable ngompa/snapcore-el7

Install snapd

    $ sudo yum install snapd

Enable snapd.socket

    $ sudo systemctl enable --now snapd.socket

Install GNOME Software snap plugin, note that GNOME Software gets replaced in this step

    $ sudo yum install gnome-software-snap

### How do I run spotify... 

run 'spotify' in your terminal

Tutorial from: https://forum.snapcraft.io/t/install-snapd-on-centos/1495/20

