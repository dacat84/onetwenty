# onetwenty

120 analoge Uhren, choreografiert – eine digitale Hommage an kinetische Uhrenkunst.

Inspiriert von *A million Times* von [Humans since 1982](https://www.humanssince1982.com). Dies ist ein privates Nachbau-/Lernprojekt ohne Verbindung zum Studio.

**Live:** https://dacat84.github.io/onetwenty/

## Was es macht

- Raster aus 8 × 18 = 144 Uhren mit je zwei Zeigern
- Die Zeiger formen die aktuelle Uhrzeit (HH:MM) in einer Konturschrift: jede Ziffer ist der Umriss eines 3 × 5-Pixel-Bitmaps, daher braucht jede Uhr genau zwei Zeiger
- Zwischendurch laufen Choreografien, gruppiert in Programme (Aktiv-/Demo-Modus spielt nur das gewählte Programm):

| Programm | Choreografien |
|---|---|
| Geometrisch | **Zahnräder** (je 4 Uhren bilden ein Achteck/Kreis; Ratschenbewegung, Nachbarn gegenläufig), **Ringe** (4 × 4-Blöcke mit großem und kleinem Kreis, gegenläufig verdrillt), **Inseln** (Umrisse wachsender und verschmelzender Inseln), **Spirale**, **Leben** (Conways Game of Life als Umrisse), **Zellen** (konzentrische Kreise um wandernde Keime) |
| Organisch | **Schwarm**, **Magnetfeld** (Eisenspäne um wandernde Pole), **Kaleidoskop**, **Moiré** (zwei überlagerte Wirbel), **Strömung**, **Atem** |
| Klassisch | Welle, Uhrwerk, Wirbel, Blüte, Schere, Diagonalen |

Organische Muster sind kontinuierliche Strömungsfelder; die Zeiger folgen ihnen mit Trägheit und Höchstdrehzahl wie echte Schrittmotoren.

## Materialien

17 Looks, wählbar in der Bedienleiste oder per `?theme=…`:

| Schlüssel | Material | Schlüssel | Material |
|---|---|---|---|
| `white` | Weiß | `nero` | Marmor Nero |
| `black` | Schwarz | `verde` | Marmor Verde |
| `neo` | Neobrutalismus lila/gelb | `rosa` | Marmor Rosa |
| `neoPink` | Neobrutalismus pink/mint | `sodalith` | Marmor Blau |
| `walnut` | Nussbaum | `copper` | Kupfer |
| `oak` | Eiche | `verdigris` | Grünspan |
| `corten` | Rost (Corten) | `concrete` | Beton |
| `carrara` | Marmor Carrara | `midnight` | Mitternacht |
| `sand` | Sandstein | | |

Holz, Marmor, Rost, Kupfer, Grünspan, Beton und Sandstein werden beim Laden prozedural aus Perlin-Rauschen erzeugt – jede Platte ist ein Unikat. Im Neo-Stil leuchten die Uhren, die gerade eine Ziffer bilden, weiß auf.

## Modi

| Modus | Verhalten |
|---|---|
| Aktiv | Uhrzeit, ab Sekunde 27 eine Choreografie, zur neuen Minute wieder die Uhrzeit |
| Demo | Choreografien laufen im Schnelldurchlauf hintereinander |
| Minimal | Nur die Uhrzeit, ohne Choreografien |

URL-Parameter: `?mode=demo`, `?theme=walnut`, `?program=geometrisch` usw.

## PCT-Starts

Der Button „PCT-Starts“ in der Bedienleiste zeigt nacheinander die Tage bis zu vier PCT-Starttagen (28.03., 17.04., 22.04. und 30.04.2027), jeweils mit Beschriftung und Datum unter der Platte; danach kehrt die Uhrzeit zurück. Vergangene Termine fallen automatisch weg. Die Termine stehen im Skript in `COUNTDOWNS`.

## Technik

Eine einzige `index.html` mit Canvas und Vanilla JS, ohne Build-Schritt. Wird direkt über GitHub Pages ausgeliefert.
