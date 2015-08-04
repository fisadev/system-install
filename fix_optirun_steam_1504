#!/bin/bash

# create a temporary directory
mkdir SteamFixTempDir
cd ./SteamFixTempDir

wget http://snapshot.debian.org/archive/debian/20140810T163814Z/pool/main/libd/libdrm/libdrm-intel1_2.4.56-1_i386.deb
wget http://snapshot.debian.org/archive/debian/20140810T163814Z/pool/main/libd/libdrm/libdrm-intel1_2.4.56-1_amd64.deb

#  32-bit
# unpack the .deb and unarchive data.tar.xz
ar p libdrm-intel1_2.4.56-1_i386.deb data.tar.xz | tar xvJ
# copy the library and link
cp ./usr/lib/i386-linux-gnu/* ~/.steam/steam/ubuntu12_32/

#  64-bit
# unpack the .deb and unarchive data.tar.xz
ar p libdrm-intel1_2.4.56-1_amd64.deb data.tar.xz | tar xvJ
# copy the library and link
cp ./usr/lib/x86_64-linux-gnu/* ~/.steam/steam/ubuntu12_64/

# cleanup
cd ..
rm -rf ./SteamFixTempDir 
