
Zde je ukázka, jak zobrazovat české znaky (UTF-8) na displejích pomocí GxEPD2 (a všude jinde, kde se používají Adafruid GFX fonty).

![Výsledek na ePaper displeji](img/epd.jpg "Výsledek na ePaper displeji")

Aby to fungovalo, musíte udělat dvě věci
- Zkonvertovat TTF font do formátu Adafruit GFX fontu, ale i s českými znaky v kódování ISO-8859-2. Na to je potřeba osmibitový fontconvert, adresář [fontconvert8](fontconvert8) .
- Vložit do Arduino kódu nástroj, který konvertuje češtinu UTF-8 na ISO-8859-2. To je v adresáři [ESP32-sample-code](ESP32-sample-code)

Vše je odvozeno od práce zveřejněné zde:
https://www.sigmdel.ca/michel/program/misc/gfxfont_8bit_en.html

Pokud si potřebujete vzniklý GFX font upravit (např. doplnit znak "stupeň" atd.), doporučuji tenhle nástroj:
https://tchapi.github.io/Adafruit-GFX-Font-Customiser/

