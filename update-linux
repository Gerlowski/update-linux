#!/bin/bash
# if not root, run as root
if (( $EUID != 0 )); then
    sudo /home/jb/bash/update.sh
    exit
fi
apt-get update
apt-get -y upgrade
apt-get -y dist-upgrade
apt-get clean
apt-get -y autoremove
apt purge -y $(dpkg -l | awk '/^rc/ { print $2 }')
