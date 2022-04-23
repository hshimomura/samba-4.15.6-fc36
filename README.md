# samba-4.15.6-fc36
Samba 4.15.6 packages for Fedora 36

As for April 23 2022, Samba 4.16 of Fedora 36 cannot share [homes] directory correctly. When you connect your Samba server running on Fedora 36, you will not see your homes directly.
Looks Samba 4.15.x train doesn't have the issue, hence I bollow Samba 4.15.x SPEC file from Fedora 35 release, mix with the latest Samba 4.15.6 code and modify for Fedora 36 release. 

# Install packages
Run like followings where packages you downloaded.

sudo dnf localinstall  samba-4.15.6-1hs.fc36.x86_64.rpm  libwbclient-4.15.6-1hs.fc36.x86_64.rpm python3-samba-4.15.6-1hs.fc36.x86_64.rpm python3-samba-dc-4.15.6-1hs.fc36.x86_64.rpm  samba-common-tools-4.15.6-1hs.fc36.x86_64.rpm  samba-dc-libs-4.15.6-1hs.fc36.x86_64.rpm samba-libs-4.15.6-1hs.fc36.x86_64.rpm  samba-client-4.15.6-1hs.fc36.x86_64.rpm  samba-client-libs-4.15.6-1hs.fc36.x86_64.rpm samba-common-4.15.6-1hs.fc36.noarch.rpm samba-common-libs-4.15.6-1hs.fc36.x86_64.rpm libsmbclient-4.15.6-1hs.fc36.x86_64.rpm


# To prevent Fedora official repo for Samba
Fedora 36 repo has newer Samba packages. If you want to keep 4.15.6, add following ecludepkgs on your /etc/dnf/dnf.conf
excludepkgs=samba* python3-samba* libsmbclient* libwbclient*

I know so far Fedora team will resolve the issue. Please delete 4.15.6 packages and use official packages.
