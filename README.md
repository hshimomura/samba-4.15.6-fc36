# samba-4.15.6-fc36
Samba 4.15.6 packages for Fedora 36

As for April 23 2022, Samba 4.16 of Fedora 36 cannot share [homes] directory correctly. When you connect your Samba server running on Fedora 36, you will not see your homes directly.
Looks Samba 4.15.x train doesn't have the issue, hence I bollow Samba 4.15.x SPEC file from Fedora 35 release, mix with the latest Samba 4.15.6 code and modify for Fedora 36 release. 

I know so far Fedora team will resolve the issue. 
Fedora 36 repo has newer Samba packages. If you want to keep 4.15.6, add following ecludepkgs on your /etc/dnf/dnf.conf



excludepkgs=samba* python3-samba* libsmbclient* libwbclient*
