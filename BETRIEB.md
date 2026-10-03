# Projektpflege und Veröffentlichung

Stand: 03.10.2026 · Version 0.22.4.

Dieses öffentliche Repository enthält die Projektbeschreibung und Dokumentation. Es enthält keine ausführbare Website und aktiviert kein GitHub Pages. Die Entwicklung wird in einem getrennten privaten Repository gepflegt. Ausgelieferter Browsercode bleibt beim späteren Website-Aufruf einsehbar; private Entwicklung ist keine Kopiersperre. Drittkomponenten behalten ihre Lizenzen und Quellpflichten.

## Vorgesehener Hostingweg

Cloudflare Pages Free, zunächst eine vom Dienst vergebene pages.dev-Adresse. Eigene Domain später; derzeit wurde keine Domain registriert und kein kostenpflichtiger Tarif eingerichtet. Cloudflare-Anmeldung und tatsächlicher Deploy sind noch offen.

Das vorbereitete statische Paket enthält 597 Dateien. Die größte Datei ist 16 MiB groß. Das HarfBuzz-Quellarchiv wurde von etwa 31,4 auf 15,5 MiB verlustfrei umkomprimiert; der entpackte Inhalt blieb per SHA-256 identisch. `.nojekyll` bleibt enthalten, hebt aber keine Hostinggrenze auf.

## Cloudflare-Git-Build vorbereiten

Das private Repository `rud5vision/pixel-und-druck-app` wird ausschließlich für Pages freigegeben. Buildbefehl: `node scripts/build-cloudflare.mjs`; Ausgabeverzeichnis: `dist`; Produktionsbranch: `main`; Framework: None; Repository-Wurzel. `.node-version` legt den lokal geprüften Node-Stand 24.19.0 fest. Mit `SKIP_DEPENDENCY_INSTALL=1` entfällt eine unbenötigte Paketinstallation.

Vor dem Build werden in Produktion und Vorschau `LEGAL_PROFILE_JSON` mit der bestätigten Betreiber-/Hostingkonfiguration und `SITE_ORIGIN` mit der echten stabilen Produktionsadresse gesetzt. Das JSON wird im Arbeitsspeicher eingelesen; lokale Konfigurationsdateien und Zugangsdaten kommen nicht ins Repository. Die vorgesehenen Betreiberangaben erscheinen trotzdem in den ausgelieferten Rechtstexten. Das Konfigurationsfeld ist kein Speicher für Passwörter oder API-Token.

Der Einstieg erzwingt die öffentlichen Buildprüfungen auch bei Vorschauen. Fehlende Angaben verhindern den Build. `SITE_INDEXABLE=false` bleibt der erste Stand; `true` kann nur den Branch `main` indexierbar machen. Vorschau-Branches bleiben gesperrt. Die temporäre `CF_PAGES_URL` wird nicht als Canonical verwendet. Erst die tatsächlich vom Host bestätigte Adresse einsetzen. Der Einstieg ist lokal in simulierten Cloudflare-Umgebungen geprüft; eine Ausführung bei Cloudflare und ein Website-Deploy stehen noch aus.

## FFmpeg-Quellenstand

Der eigene FFmpeg-Neubuild ist erfolgreich erstellt, geprüft und eingebaut. 17 originale Quellarchive, die SDL2-Portquelle und 29 Lizenztexte stimmen mit den ausgeführten Build-Eingaben überein. Eine zusätzliche ZIP-Datei enthält das tatsächlich verwendete Rezept, Vorbereitung/Buildskripte, Compiler-/Konfigurationsnachweise und Medienprüfungen. Das Paket wurde separat rekonstruiert und gegen alle 18 Archive geprüft. Der ausgeführte Neubuild erzeugt JavaScript und WASM bytegleich zum bisherigen Encoder. Technische Quellen-/Binärzuordnung ist damit für diesen Ersatz belegt; dies ist keine rechtliche Gesamtfreigabe oder nachträgliche Bestätigung des früheren npm-Binärpakets. APT und BuildKit sind nicht eingefroren; kein bitidentischer Neubuild zugesagt. Quellenarchive laden erst auf ausdrücklichen Aufruf, nicht beim Seitenstart.

## Aktualisieren

1. Quelle ändern. `dist/*.mjs` sind zum Teil echte Quellen; den Ordner nicht pauschal löschen.
2. Lokal bauen und die betroffenen Funktionen einschließlich echter Ausgaben prüfen. Zwölf Sprachen und vorhandene Werkzeuge erhalten.
3. Für Cloudflare am Root-Pfad `/` bauen. Nach Vergabe der tatsächlichen Adresse `SITE_ORIGIN` darauf setzen. Keine Beispieldomain verwenden.
4. Vor Indexfreigabe Betreiber-/Hostingprofil abschließen; die geprüfte FFmpeg-Quellenzuordnung beim Update erhalten. `SITE_INDEXABLE=true` und `PUBLIC_RELEASE=true` sind eigene, überprüfte Freigabeschritte. Der Build prüft jetzt beide Quellennachweise zusätzlich zum Betreiberprofil und zur echten Websiteadresse.
5. Geprüften Stand veröffentlichen. Deploymentstatus und ausgelieferte Version kontrollieren; danach Canonical, Sprachverweise und Sitemap überprüfen.
6. README, Formate und Änderungsverlauf zusammen aktualisieren. Private Konfigurationen, Zugangsdaten, Nutzermedien und Testdateien bleiben außerhalb dieser öffentlichen Dokumentation.

## Suchdaten und Werbung

156 vorhandene Sprach-/Aufgabenseiten werden Suchkandidaten zugeordnet. Eine allgemeine Web-Suchprobe ist keine gemessene Google-Platzierung und kein Suchvolumen. Search Console muss nach Veröffentlichung verifiziert werden; eigene Nutzungs-, Ranking- und Umsatzdaten liegen noch nicht vor.

Die Anwendung bindet derzeit keine Werbung, Trackingintegration, Zahlungsdienste oder Versandfunktion ein. Ein späterer Werbestart benötigt die dazu passenden Betriebs- und Datenschutzangaben. Nutzerdateien bleiben lokal.

## Abschalten

Eine spätere Website-Veröffentlichung lässt sich beim Host aufheben. Bereits entstandene Fremdkopien oder Suchmaschinen-Caches sind damit nicht automatisch entfernt. Das öffentliche Projektprofil kann unabhängig von der Website gepflegt werden.

Offizielle Grundlagen: [Cloudflare-Git-Anbindung](https://developers.cloudflare.com/pages/configuration/git-integration/), [Cloudflare-Limits](https://developers.cloudflare.com/pages/platform/limits/), [Google Search Console](https://developers.google.com/search/docs/monitor-debug/search-console-start).
