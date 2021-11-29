Konverze TTF fontu na font pro Adafruit GFX library - včetně češtiny v ISO 8859-2 (Latin 2). Místo standardní konverze jen sedmibitových znaků konvertuje znaky osmibitové..

Kód vychází z práce zveřejněné zde:
https://www.sigmdel.ca/michel/program/misc/gfxfont_8bit_en.html

Sestavení na Ubuntu 18:

1) Je potřeba mít make a gcc
```console
sudo apt install make
sudo apt install gcc
```

2) Je potřeba mít knihovnu freetype včetně hlaviček
```console
sudo apt install libfreetype6
sudo apt install libfreetype6-dev
```

3) Pak už to jde sestavit
```console
make -f Makefile8
```

4) A použít:
```console
./fontconvert8 myFonts/FreeSans.ttf 9 > myFonts/FreeSans9pt.h
```

DPI displeje se nastaví na řádce 77 v fontconvert8.c
```cpp
#define DPI 141 // Approximate res. of Adafruit 2.8" TFT
```



