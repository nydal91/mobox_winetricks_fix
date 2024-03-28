wrtite in termux : 


Winetricks
LD_PRELOAD= WINESERVER=$PREFIX/glibc/wine/bin/wineserver WINE=$PREFIX/glibc/wine/bin/wine $PREFIX/glibc/bin/box64 $PREFIX/glibc/bin/bash86 $PREFIX/glibc/wine/bin/winetricks
