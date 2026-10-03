# Projektpflege und Veröffentlichung

Stand: 03.10.2026 · Version 0.22.3.

Dieses öffentliche Repository enthält die Projektbeschreibung und Dokumentation. Es enthält keine ausführbare Website und aktiviert kein GitHub Pages. Die Entwicklung wird in einem getrennten privaten Repository gepflegt. Ausgelieferter Browsercode bleibt beim späteren Website-Aufruf einsehbar; private Entwicklung ist keine Kopiersperre. Drittkomponenten behalten ihre Lizenzen und Quellpflichten.

## Vorgesehener Hostingweg

Cloudflare Pages Free, zunächst eine vom Dienst vergebene pages.dev-Adresse. Eigene Domain später; derzeit wurde keine Domain registriert und kein kostenpflichtiger Tarif eingerichtet. Cloudflare-Anmeldung und tatsächlicher Deploy sind noch offen.

Das vorbereitete statische Paket enthält 595 Dateien. Die größte Datei ist 16 MiB groß. Das HarfBuzz-Quellarchiv wurde von etwa 31,4 auf 15,5 MiB verlustfrei umkomprimiert; der entpackte Inhalt blieb per SHA-256 identisch. `.nojekyll` bleibt enthalten, hebt aber keine Hostinggrenze auf.

## FFmpeg-Quellenstand

17 Quellarchive, die zusätzliche SDL2-Portquelle und 29 separat zugängliche Lizenztexte sind per Hash geprüft. Ein Ersatzrezept mit festen Quellständen und SDK-Image-Digest wurde vorbereitet. Der Ersatz wurde noch nicht kompiliert, eingebaut oder veröffentlicht; die ursprüngliche genaue Binär-/Quellenzuordnung bleibt offen. Quellenarchive laden erst auf ausdrücklichen Aufruf; sie gehören nicht zu den Ressourcen beim Seitenstart.

## Aktualisieren

1. Quelle ändern. `dist/*.mjs` sind zum Teil echte Quellen; den Ordner nicht pauschal löschen.
2. Lokal bauen und die betroffenen Funktionen einschließlich echter Ausgaben prüfen. Zwölf Sprachen und vorhandene Werkzeuge erhalten.
3. Für Cloudflare am Root-Pfad `/` bauen. Nach Vergabe der tatsächlichen Adresse `SITE_ORIGIN` darauf setzen. Keine Beispieldomain verwenden.
4. Vor Indexfreigabe Betreiber-/Hostingprofil und FFmpeg-Quellenzuordnung abschließen. `SITE_INDEXABLE=true` und `PUBLIC_RELEASE=true` sind eigene, überprüfte Freigabeschritte. Der Build prüft jetzt beide Quellennachweise zusätzlich zum Betreiberprofil und zur echten Websiteadresse.
5. Geprüften Stand veröffentlichen. Deploymentstatus und ausgelieferte Version kontrollieren; danach Canonical, Sprachverweise und Sitemap überprüfen.
6. README, Formate und Änderungsverlauf zusammen aktualisieren. Private Konfigurationen, Zugangsdaten, Nutzermedien und Testdateien bleiben außerhalb dieser öffentlichen Dokumentation.

## Suchdaten und Werbung

156 vorhandene Sprach-/Aufgabenseiten werden Suchkandidaten zugeordnet. Eine allgemeine Web-Suchprobe ist keine gemessene Google-Platzierung und kein Suchvolumen. Search Console muss nach Veröffentlichung verifiziert werden; eigene Nutzungs-, Ranking- und Umsatzdaten liegen noch nicht vor.

Die Anwendung bindet derzeit keine Werbung, Trackingintegration, Zahlungsdienste oder Versandfunktion ein. Ein späterer Werbestart benötigt die dazu passenden Betriebs- und Datenschutzangaben. Nutzerdateien bleiben lokal.

## Abschalten

Eine spätere Website-Veröffentlichung lässt sich beim Host aufheben. Bereits entstandene Fremdkopien oder Suchmaschinen-Caches sind damit nicht automatisch entfernt. Das öffentliche Projektprofil kann unabhängig von der Website gepflegt werden.

Offizielle Grundlagen: [Cloudflare-Git-Anbindung](https://developers.cloudflare.com/pages/configuration/git-integration/), [Cloudflare-Limits](https://developers.cloudflare.com/pages/platform/limits/), [Google Search Console](https://developers.google.com/search/docs/monitor-debug/search-console-start).
