# Fedora-Kinoite-how-to
Guide from me for me, for using Fedora Kinoite


## Hide Firefox:

$ sudo mkdir -p /usr/local/share/applications/

$ sudo cp /usr/share/applications/firefox.desktop /usr/local/share/applications/

$ sudo sed -i "2a\\NotShowIn=GNOME;KDE" /usr/local/share/applications/firefox.desktop

$ sudo update-desktop-database /usr/local/share/applications/

## Make Firefox flatpak use wayland:

flatpak override --user --env=MOZ_ENABLE_WAYLAND=1 org.mozilla.firefox

## Hardware video acceleration for Firefox flatpak:

about:config:

gfx.webrender.all --> true

media.ffmpeg.vaapi.enabled --> true

## Stop some services:
From: https://yorickpeterse.com/articles/switching-to-fedora-silverblue/

sudo systemctl stop systemd-oomd

sudo systemctl disable systemd-oomd

sudo systemctl mask systemd-oomd

Stoping firewall (optional):
sudo systemctl disable firewalld

## SDDM big cursor size (F38):

sudo nano /etc/environment

copy/paste: XCURSOR_SIZE=24
