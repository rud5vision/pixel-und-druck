# Werkzeuge und Formate · 0.22.2

Die Dateiendung beschreibt einen Container oder Dateityp. Enthaltene Codecs, Farbmodelle, Verschlüsselung und Geräteleistung bestimmen zusätzlich, ob eine konkrete Datei funktioniert. Diese Liste ist keine Garantie für jede Variante.

| Bereich | Einlesen | Speichern / Ergebnis |
| --- | --- | --- |
| Bildkonverter | JPG, PNG, WebP, GIF, BMP, TIFF, PDF, Krita `.kra`, OpenRaster `.ora` | JPG, PNG, WebP, GIF als Einzelbild, PDF als Rasterbild, TIFF, BMP, ORA mit einer zusammengeführten Ebene |
| PDF-Organizer | Unterstützte PDFs, einschließlich passwortgeschützter Dateien mit bekanntem Passwort | Zusammenfügen, Seiten auswählen, sortieren, drehen und teilen; PDF-Kopie mit Text/Vektoren soweit unterstützt |
| PDF-/Ebenenauswahl | PDF-Seiten, ORA-PNG-Ebenen, unterstützte KRA-v2-Rasterebenen (RGB/Grau 8/16 Bit) | Einzelne Ebene/Seite übernehmen; PNG-ZIP; ausgewählte Original-PDF-Seiten kopieren |
| GIF & Animation | GIF; animiertes WebP bei vorhandenem Browserdecoder | Zeitbereich, Tempo, Richtung, Wiederholung und Größe; Gesamtanimation als GIF, einzelne PNGs und PNG-ZIP |
| Video & Audio | Unter anderem MP4, MOV, MKV, WebM, AVI, MPEG, WMV, FLV, MTS, MXF, MP3, WAV, FLAC, AAC | MP4, WebM, MOV, MKV, AVI, MPEG, WMV, FLV, 3GP, TS, OGV, GIF, animiertes WebP, MP3, WAV, FLAC, AAC/ADTS, M4A, OGG/Vorbis und Opus/Ogg |
| Wallpaper | Gemeinsame Bildquelle oder übernommenes Einzelbild | Monitorformate, eigene Pixelmaße, Zuschnitt, Ränder, Zoom; JPG, PNG, WebP |
| Fotobogen | Gemeinsame Bildquelle oder ausgewählte PDF-Seite/Ebene | Ein Foto mehrfach auf einem Blatt; eigene Maße, Papierformat, Ränder, Beschnitt; JPG, PNG oder PDF |
| Druck und Maße | Bildmaße oder manuelle Pixel-/Längeneingabe | Druckgröße, PPI-Prüfung, Formatvergleich, Beschnitt-/Randvorschau und Download |

## Unterschiede, die wichtig sind

- **WebM** ist ein Video-/Audiocontainer; **WebP** ist ein Bildformat mit möglicher Animation. Animiertes WebP wird im GIF-Bereich geöffnet. Video kann als animiertes WebP ausgegeben werden.
- **PPI** steuert die physische Druckgröße. 600 PPI statt 300 PPI erzeugt bei gleichen Pixelmaßen keine neuen Details. Wallpaper verwendet Pixelmaße.
- **PDF als Bild** rastert eine ausgewählte Seite. Der **PDF-Organizer** kopiert dagegen Seiteninhalte. Formulare, Signaturen und Lesezeichen sind nicht allgemein zugesichert.
- **Passwort-PDFs:** bekannte Passwörter werden lokal verarbeitet. Neue Exporte haben keinen Passwortschutz. Zertifikats-/DRM-Schutz und beliebige andere verschlüsselte Formate sind nicht zugesichert.
- **Krita-Ebenen** ersetzen keinen Krita-Renderer. Masken, Effekte, Mischmodi, Ebenendeckkraft und ICC-Umwandlung werden beim einzelnen Rasterebenenexport nicht vollständig berücksichtigt.
- **Umpacken** kopiert kompatible Spuren ohne Neukodierung. Schnitt, Drehung und andere Änderungen können Neukodierung benötigen. AV1/VP9 und weitere Browser-Codecs hängen vom Gerät ab.
- **GIF** begrenzt die Farben und unterstützt keine weiche Teiltransparenz. Einzelbild-Konvertierung und Gesamtanimation sind unterschiedliche Aufgaben.
- **Fotomaße** sind keine biometrische Zulassung. Für deutsche Ausweise/Reisepässe ersetzt ein selbst gedruckter Bogen den vorgeschriebenen digitalen Übermittlungsweg nicht; der Toolhinweis verlinkt die Behördeninformationen.

## Gerätegrenzen

Bildausgabe maximal 128 Megapixel und 16.000 Pixel je Kante; kleinere Browsergrenzen sind möglich. Ab 24 MP erscheint ein Speicherhinweis. Vorschau und Export arbeiten mit unterschiedlichen Auflösungen; exportiert wird aus der Originalquelle. Downloads zeigen vor dem Speichern die tatsächlich erzeugte Dateigröße.

Große PDF-, Animations- und Videoaufgaben besitzen weitere sichtbare Grenzen. Chromium, Firefox und die Playwright-WebKit-Engine wurden unter Windows mit acht Bild-/Dokumentformaten, GIF, Passwort-PDF sowie MP4/WebM/MP3 geprüft. Das getestete WebKit besitzt keinen Decoder für animiertes WebP; hierfür erscheint ein konkreter Browserhinweis. Physische Handys und sämtliche Safari-/Firefox-Varianten sind nicht allgemein abgenommen.
