


# Installation of Spotify


![enter image description here](https://i2-prod.mirror.co.uk/incoming/article2878879.ece/ALTERNATES/s615/spotifynew_large_verge_medium_landscape.jpg)


----------


#####  Install the COPR plugin and EPEL

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
Or search for the App in your applications

