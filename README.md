export GLIBC_BIN=$PREFIX/glibc/bin
pkg install cabextract unzip p7zip which

# download bash for x86
wget https://github.com/ptitSeb/box64/raw/main/tests/bash
mv bash $GLIBC_BIN/bash86
chmod +x $GLIBC_BIN/bash86

# download winetricks
wget https://raw.githubusercontent.com/Winetricks/winetricks/master/src/winetricks
mv winetricks $GLIBC_BIN/winetricks
chmod +x $GLIBC_BIN/winetricks

wrtite in termux : 


Winetricks
LD_PRELOAD= WINESERVER=$PREFIX/glibc/wine/bin/wineserver WINE=$PREFIX/glibc/wine/bin/wine $PREFIX/glibc/bin/box64 $PREFIX/glibc/bin/bash86 $PREFIX/glibc/wine/bin/winetricks
