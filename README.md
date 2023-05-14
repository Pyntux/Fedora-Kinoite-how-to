# Fedora-Kinoite-how-to
Guide from me for me, for using Fedora Kinoite


### Hide Firefox:

$ sudo mkdir -p /usr/local/share/applications/
$ sudo cp /usr/share/applications/firefox.desktop /usr/local/share/applications/
$ sudo sed -i "2a\\NotShowIn=GNOME;KDE" /usr/local/share/applications/firefox.desktop
$ sudo update-desktop-database /usr/local/share/applications/
