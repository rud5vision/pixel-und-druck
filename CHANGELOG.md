# Änderungen

## 0.22.3 · 03.10.2026

- SDL2-Portquelle ergänzt und gegen den SHA-512 des Emscripten-Ports geprüft.
- 29 unveränderte Lizenztexte der FFmpeg-Abhängigkeiten und des SDK separat mit Herkunft und Hash verlinkt.
- Ersatzrezept mit festen Quellständen, SDK-Image-Digest und Compilerflags vorbereitet. Archiv- und Kontextprüfung funktioniert unter Windows; interne Verknüpfungen bleiben innerhalb der Quellen.
- Sieben Prüfungen der sicheren Buildvorbereitung bestanden. Noch kein Compilerlauf, Austausch des Encoders oder Website-Deploy.
- 70 Logik- und Buildtests bestanden; sämtliche Werkzeuge und zwölf Sprachen erhalten. Die Medien- und Layoutbelege aus 0.22.2 bleiben Belege für den unveränderten Encoder.

## 0.22.2 · 03.10.2026

- GIF-Vorschau ohne Worker-Canvas ermöglicht; GIF-Export in Firefox repariert. Vorschau und Export greifen geordnet auf den Decoder zu.
- Abbruch, erneuter Export sowie Transparenz und Bildüberlagerungen in drei Browser-Engines geprüft.
- Kontraste im Druck-Zuschnitt und im PPI-Symbol verbessert; Wallpaper-Vorschau für Hilfstechnologien korrekt bezeichnet.
- Piko und Neuigkeiten in allen zwölf Sprachen aktualisiert.
- Öffentlicher Build stoppt auch bei unvollständigen FFmpeg-Quellennachweisen.
- 67 automatisierte Logiktests, 81 Layoutansichten, 27 automatisierte Zugänglichkeitsprüfungen und 46 unabhängig dekodierte Ausgabedateien bestanden. Physische Handys bleiben offen.

## 0.22.1 · 03.10.2026

- Zielhosting wieder auf Cloudflare Pages Free ausgerichtet; lokale Rechtstexte behaupten keinen erfolgten GitHub-Deploy.
- HarfBuzz-Quellarchiv verlustfrei unter die Cloudflare-Dateigrenze gebracht.
- Bestehende Sprach-/Aufgabenseiten einer ersten Suchmatrix zugeordnet; keine gemessenen Suchvolumen oder Rankings behauptet.
- Öffentliche Projektbeschreibung aktualisiert. Umfang der Werkzeuge bleibt erhalten.


## 0.22.0 · 3. Oktober 2026

- GitHub-Projektpfade für Sprache, Szenarien, Vorschauen, Bibliotheken und Worker berücksichtigt. `.nojekyll` wird mitgeliefert.
- Piko verlinkt Impressum, Datenschutz, Rechte und den aktuellen GitHub-Projektstand. Kontextbezogene Hilfe und lokale Feedbackentwürfe bleiben erhalten.
- Datenschutz erklärt PDF-Passwörter, entschlüsselte Arbeitskopien und GitHub-Hosting. Die Rechtstexte sind weiterhin als unvollständiger Entwurf gekennzeichnet.
- Quellarchive und Buildrezept der FFmpeg-Komponenten ergänzen die vorhandenen Lizenztexte. Eine vollständige Reproduktion des fremden Binärpakets ist nicht belegt.
- README und Formatübersicht bilden den aktuellen Werkzeugumfang ab.

## 0.21.5

GIF-/WebP-Vorschau beachtet Wiederholungswahl und ursprüngliche Schleifenzahl. Schnelles Stoppen/Starten erzeugt keine parallelen Wiedergabeschleifen. „Gesamte Animation“ setzt die Vorschau zurück. GIF-Schaltflächen im Dark Mode, Eingabeformat-Beschriftungen und aktuelle Kataloghinweise korrigiert.

## 0.21.4

Passwortgeschützte PDFs mit bekanntem Passwort lokal öffnen. Falsches Passwort, Abbruch und erneute Auswahl werden behandelt. Neue Exporte sind ungeschützt; das Original bleibt unverändert.

## 0.21.3 und frühere Ausbaustufen

28 Werkzeug-Einstiege, Video-/Audiokonvertierung, native Browser-Codecs und Umpacken, PDF-Organizer, Fotobögen, Krita-/OpenRaster-Ebenen, GIF-Zeitauswahl, Wallpaper, Druck-/Pixelrechner, zwölf Sprachen und System/Hell/Dunkel.

Die experimentelle Hintergrundfreistellung wurde entfernt. Sie gehört nicht zum aktuellen Funktionsumfang.
