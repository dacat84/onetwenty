# onetwenty

120 analoge Uhren, choreografiert – eine digitale Hommage an kinetische Uhrenkunst.

Inspiriert von *A million Times* von [Humans since 1982](https://www.humanssince1982.com). Dies ist ein privates Nachbau-/Lernprojekt ohne Verbindung zum Studio.

**Live:** https://dacat84.github.io/onetwenty/

## Was es macht

- Raster aus 8 × 18 = 144 Uhren mit je zwei Zeigern
- Die Zeiger formen die aktuelle Uhrzeit (HH:MM) in einer Konturschrift: jede Ziffer ist der Umriss eines 3 × 5-Pixel-Bitmaps, daher braucht jede Uhr genau zwei Zeiger
- Zwischendurch laufen Choreografien: Schwarm, Kaleidoskop, Strömung, Atem (kontinuierliche Strömungsfelder mit Perlin-Rauschen) sowie Welle, Wirbel, Diagonalen, Blüte, Schere

## Modi

| Modus | Verhalten |
|---|---|
| Aktiv | Uhrzeit, ab Sekunde 27 eine Choreografie, zur neuen Minute wieder die Uhrzeit |
| Demo | Choreografien laufen im Schnelldurchlauf hintereinander |
| Minimal | Nur die Uhrzeit, ohne Choreografien |

URL-Parameter: `?mode=demo`, `?theme=black`

## Technik

Eine einzige `index.html` mit Canvas und Vanilla JS, ohne Build-Schritt. Wird direkt über GitHub Pages ausgeliefert.
