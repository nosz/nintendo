**🎮 Live ansehen: [https://nosz.github.io/nintendo](https://nosz.github.io/nintendo)**

[![Nintendo Quest: Was weißt du über Nintendo? / What do you know about Nintendo? / 任天堂、どれくらい知ってる？](nintendo_vorschau.jpg)](https://nosz.github.io/nintendo)

# NINTENDO: Nintendo Quest

**Inoffizielles Lernprojekt von Leonie Szpak**

**Datei:** `index.html` (eine Datei, offline lauffähig, Version 1.9.3, Stand 14.10.2026). Einfach im Browser öffnen oder auf einem Webserver ablegen.

## Inhalt
Dashboard mit 7 Lektionen (je 3 Info-Karten, ein Kenner-Bonus für Langjährige, Humor-Pause, Quellen, 4 bis 5 Quizfragen), Sprachen **Deutsch, Englisch, Japanisch** (Umschalter oben, wird gespeichert).

| Nr. | Lektion | Fragen |
|---|---|---|
| 1 | Blitzstart: 1889 in 60 Sekunden (2 Karten) | 2 |
| 2 | Ab in den Fernseher: Famicom und Europa (2 Karten) | 2 |
| 3 | Mario | 4 |
| 4 | Zelda | 4 |
| 5 | Handhelds und Pokémon | 4 |
| 6 | Wii, Switch, Switch 2 | 4 |
| 7 | Bossrunde | 5 |

**Startseite:** Einstieg mit der Frage "Hey, was weißt du über Nintendo?" und zwei Wegen: "Ich bin neu hier" (Level 1) und "Ich bin schon lange dabei" (direkt zur Bossrunde). Mit Fortschritt wird daraus "Weiter geht's" zur nächsten offenen Lektion. Gedacht für neue Mitarbeitende, Erfahrene und die Chefetage.

**Zertifikate:** Zu jeder bestandenen Lektion gibt es eine Urkunde im bunten Nintendo-Stil mit motivierendem Spruch (je nach Sternen), zum Abschluss aller sieben das Meister-Zertifikat. Name eingeben, als PNG speichern oder drucken (A4 quer). Auf jeder Urkunde steht, dass sie inoffiziell und kein Nintendo-Produkt ist.

**Schnelle Erfolge:** Lektion 1 und 2 sind bewusst winzig (je 2 Karten, 2 Fragen, ca. 1 bis 2 Minuten). Schon die erste richtige Antwort löst den Erfolg "Erster Treffer" aus, und auf der Ergebnisseite erscheint das Zertifikat sofort, mit Namensfeld und Speichern-Knopf. Mehr Details der gekürzten Lektionen stehen im Kenner-Bonus.

**Name und Personalisierung:** Beim ersten Start fragt die App kurz "Wie dürfen wir dich nennen?" (Eingabe optional, "Lieber anonym bleiben" möglich). Der Name wird nur lokal im Browser (`localStorage`) gespeichert, nie übertragen. Er steckt in Begrüßung, erster und letzter Quizfrage, Rückmeldungen (Treffer und Fehlversuch), Ergebnis und Zertifikat (Name plus persönlicher Spruch). Namen lassen sich über den Namens-Chip oder auf der Zertifikatsseite ändern. Ohne Namen laufen die neutralen Texte.

**Nintendo-Links:** Startseite (Abschnitt "Mehr über Nintendo": offizielle Seite je Sprache, Firmengeschichte, Unternehmensinformationen), Fußzeile, Zertifikat (Webadresse und Marke "NINTENDO QUEST") sowie Link auf Ergebnis- und Zertifikatsseite. Alle öffnen im gleichen Tab.

Spielmechanik: 10 Münzen je richtiger Antwort, 1 bis 3 Sterne je Lektion (50 %, 75 %, 100 %), 5 Ränge von "Pilz-Praktikant" bis "Legende", Konfetti bei bestandenem Level, Fortschritt im Browser gespeichert (`localStorage`), Hell- und Dunkelmodus, Tastaturbedienung, "weniger Bewegung" wird beachtet.

## PWA (installierbare App, offline)
Nintendo Quest ist eine Progressive Web App: Auf Handy und Rechner lässt sie sich wie eine App installieren (Chrome/Edge: "Installieren" auf der Startseite oder im Browser-Menü; iPhone/Safari: Teilen, dann "Zum Home-Bildschirm"), startet im eigenen Fenster mit eigenem Icon und läuft nach dem ersten Laden **ohne Internet**.
- **Dateien (alle ins Hauptverzeichnis des Repositories, ohne Unterordner):** `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `favicon.png`, `favicon.svg`, `apple-touch-icon.png`, `nintendo_vorschau.jpg`. Die Seite muss über HTTPS laufen (GitHub Pages tut das).
- **Wenn auf dem Handy statt des Icons nur ein Buchstabe (z. B. "G") erscheint:** Die Icon-Dateien (icon-192.png, icon-512.png, icon-maskable-512.png, pple-touch-icon.png, avicon.png) fehlen auf dem Server (404). Alle Dateien der Liste oben hochladen, auf dem Handy die alte Verknüpfung löschen, die Seite neu laden (ggf. Browserdaten der Seite löschen) und die Verknüpfung bzw. die App neu anlegen. Prüfung: https://nosz.github.io/nintendo/icon-192.png muss ein Bild liefern.
- **Offline:** Der Service Worker (`sw.js`) legt die Kerndateien in den Cache `nintendo-quest-<Version>`. Seiten werden zuerst aus dem Netz geholt (4 s Zeitlimit), sonst aus dem Cache.
- **Updates:** Gibt es eine neue Version, erscheint unten "Neue Version verfügbar" mit Knopf "Aktualisieren". Nach dem Klick lädt die App neu, der alte Cache wird gelöscht. **Bei jeder neuen Version `VERSION` in `index.html` und in `sw.js` gleichzeitig erhöhen** (sonst wird nichts aktualisiert).
- **Fortschritt:** Name, Sprache und Fortschritt liegen im Browser-Speicher (`localStorage`, Schlüssel `nintendo_quest_v1`) und bleiben nach Tagen, Neustart, Schließen des Tabs und App-Updates erhalten. Der Browser-Speicher gehört zur Adresse: Wer die Seite im Browser und als installierte App nutzt, hat zwei getrennte Speicherstände. Wird der Browser-Speicher für die Seite gelöscht, ist der Fortschritt weg.
- **Kopfzeile:** unter dem Namen steht "Inoffizielles Lernprojekt von Leonie Szpak".

## Veröffentlichung und Link-Vorschau
Geplante Adresse: https://nosz.github.io/nintendo/ (GitHub Pages, Repository `nintendo`, Dateien `index.html` und `nintendo_vorschau.jpg` ins Hauptverzeichnis legen). Die Vorschau (Open Graph / Twitter Card) zeigt `nintendo_vorschau.jpg` (1200 x 630, bunte Spielkarten, Sterne, Münze, kurze Fragen auf Deutsch, Englisch und Japanisch) mit dreisprachigem Kurztitel und Kurzbeschreibung. Die Bild-Adresse trägt `?v=2`, damit Messenger das neue Bild statt eines zwischengespeicherten laden (bei der nächsten Bildänderung auf `?v=3` hochzählen). Wichtig: Die Bild-Adresse in den Tags ist absolut und gilt nur unter dieser Adresse; Messenger und Netzwerke speichern Vorschauen zwischen (nach dem Hochladen ggf. mit dem Debugger der jeweiligen Plattform neu einlesen). Vor einer öffentlichen Freigabe Management/Legal einbeziehen (siehe Grenzen).

## Logo und Icons
Eigenes Logo: ein Pixel-Gamepad (original gezeichnet, kein Nintendo-Logo und keine Nintendo-Figur). Es steht in der Kopfzeile, im Siegel der Zertifikate und als Tab-Icon. Dateien im Hauptverzeichnis mit hochladen: `favicon.png` (64 px), `apple-touch-icon.png` (180 px); das SVG-Icon ist in `index.html` eingebettet (`favicon.svg` liegt zusätzlich bei). Das offizielle Nintendo-Logo und Figuren wie die Pixel-Figur aus dem Tab-Beispiel sind absichtlich nicht enthalten (Marken- und Urheberrecht); sie kämen nur nach Freigabe durch Management/Legal und mit gelieferter Originaldatei in Frage.

## Marke und Look
Stil angelehnt an die Ausrichtung von Nintendo (Rot/Weiß, runde Karten, verspielte Animationen). Es werden **keine Logos, Figurenbilder oder kopierten Texte** verwendet. Die Seite nintendo.com/de-de war in dieser Umgebung gesperrt und wurde nicht ausgewertet; der Look beruht auf allgemeinen Gestaltungsmerkmalen, nicht auf einem Abgleich mit der Seite. Gern Screenshot oder Farbwerte liefern, dann lässt sich der Look nachschärfen.

## Quellen (Stand 14.10.2026)
- Nintendo Unternehmensgeschichte: https://www.nintendo.co.jp/en/corporate/en/history/index.html (1889, 1902, 1947, 1953, 1983, 1989, 2001)
- Wikipedia: Nintendo, Mario, The Legend of Zelda, Animal Crossing (https://en.wikipedia.org/wiki/Nintendo usw.): Jahreszahlen, Verkaufszahlen, Personen
- Video Games Chronicle (Switch-2-Zahlen): https://www.videogameschronicle.com/news/switch-2-continues-to-be-nintendos-fastest-selling-system-latest-financial-results-show/

## Bekannte Grenzen
- Wikipedia und Presse sind Sekundärquellen. Verkaufszahlen ändern sich je Quartal; für offizielle Werte den Investorenbereich von Nintendo prüfen. Exakte Erscheinungstage von Breath of the Wild und Tears of the Kingdom wurden nicht verifiziert (nur Jahre).
- Der Switch-Starttermin 3. März 2017 und die Zahlen 2026 stammen aus Suchergebnissen/Presse, nicht aus einer geprüften Nintendo-Primärseite.
- **Die japanischen Texte sollten vor breiter Nutzung von Muttersprachlern geprüft werden.**
- Nur intern bei Ninox nutzen. Eine öffentliche Veröffentlichung vorher mit Management/Legal klären (Marken, Stil-Anlehnung).

## Tests (14.10.2026, lokaler Testserver)
Daten (alle Texte in DE/EN/JA, 4 Antworten je Frage), Quiz-Durchlauf je Sprache, Sprachwechsel mitten im Quiz, Rang/Fortschritt, keine `target`-Links, alle 6 externen Links HTTP 200; Zertifikate (gültiges SVG in 3 Sprachen, Text innerhalb des Rands, PNG-Erzeugung, Name live), Startseite (Einstiege, Fortschrittslogik), Blitzlektionen (Erfolg nur einmal, Zertifikat sofort, 0 richtig = kein Zertifikat); UX-Suite U1 bis U10 mobil (375 px) hell und dunkel bestanden. Das Speichern als PNG wurde per Canvas geprüft, nicht der Download-Dialog. Nicht getestet: echtes Gerät, Server-Betrieb, Offline-Cache (kein Service Worker eingebaut).

## Änderungsprotokoll
- 1.0.0 (14.10.2026): Erstfassung.
- 1.1.0 (14.10.2026): Zertifikate je Lektion und Meister-Zertifikat (DE/EN/JA, PNG, Druck).
- 1.2.0 (14.10.2026): Neue Startseite: Einstiegsfrage, zwei Wege (neu / lange dabei), kompakter Kopfbereich.
- 1.9.2 (14.10.2026): Icons liegen im Hauptverzeichnis (der Ordner icons/ war auf dem Server nicht vorhanden: Android zeigte nur einen Buchstaben statt des Icons, der Service Worker brach beim Installieren ab). Service Worker robuster: nur index.html und Manifest sind Pflicht, Icons und Bild sind optional. Zusätzliche Icon-Links (192, 512, 180) im Kopf.
- 1.9.1 (14.10.2026): Hinweis in der Fußzeile nennt Leonie Szpak (DE/EN/JA).
- 1.9.0 (14.10.2026): Professionelle PWA: Manifest (Name, Icons 192/512/maskable, Shortcuts, Kategorien), Service Worker mit Offline-Cache und Update-Hinweis, Installieren-Karte (iPhone-Hinweis), Offline-Bereit-Meldung, Safe-Area für Geräte mit Notch. Kopfzeile: 'Inoffizielles Lernprojekt von Leonie Szpak' unter dem Namen; Münzzähler auf dem Handy ausgeblendet (steht in der Startseiten-Kachel).
- 1.8.0 (14.10.2026): Startseite professioneller (Statistik-Kacheln für Rang, Münzen, Sterne; kompakte Lektionsliste auf dem Handy mit markierter nächster Lektion und Fortschrittszähler; Namen-ändern-Knopf). Ganz oben eine Zeile 'Inoffizielles Lernprojekt von Leonie Szpak' (auch auf dem Zertifikat), in DE/EN/JA.
- 1.7.1 (14.10.2026): Benutzerführung: Zurück-Knopf mit klarem Pfeil-Symbol (44 px, Rahmen) und kurzer Beschriftung (Übersicht / Zur Lektion) plus Lektionstitel als Kontext; Ergebnisseite mit eindeutigem Hauptknopf (Nächste Lektion, sonst Wiederholen/Speichern), übrige Knöpfe zurückhaltend.
- 1.7.0 (14.10.2026): Eigenes Pixel-Gamepad als Logo (Kopfzeile, Zertifikat-Siegel, Tab-Icon, Apple-Icon) statt Stern.
- 1.6.0 (14.10.2026): Beim ersten Quiz fragt ein kurzer Boxenstopp nach dem Namen (falls noch keiner gesetzt ist, einmalig, überspringbar). Vorschaubild und Vorschautexte dreisprachig (DE/EN/JA) und kürzer.
- 1.5.0 (14.10.2026): Namensabfrage am Start, Personalisierung (Begrüßung, Quiz, Ergebnis, Zertifikat), kompakter Handy-Kopf mit Segment-Sprachwahl, feste Aktionsleiste in Lektionen, volle Knopfbreite auf Ergebnis- und Zertifikatsseite, Namensbreite auf der Urkunde berechnet.
- 1.4.0 / 1.4.1 (14.10.2026): Nintendo auf dem Zertifikat (Marke, Webadresse) und Nintendo-Links auf der Oberfläche.
- 1.3.1 (14.10.2026): Überschriftenebene in Lektionen korrigiert (h2), leerer Fortschritt bei 0 richtig vermieden; Link-Vorschau (Open Graph, Twitter Card), Vorschaubild, Favicon; Datei in index.html umbenannt.
- 1.3.0 (14.10.2026): Lektion 1 und 2 auf je 2 Karten und 2 Fragen gekürzt, Erfolg bei der ersten richtigen Antwort, Zertifikat direkt auf der Ergebnisseite, goldene Sterne im Ergebnis.
- 1.9.3 (14.10.2026): Fix: Wer den Namen leer oder nur mit Leerzeichen bestätigt, kann ihn später über „Name eintragen“ auf der Startseite nachholen.
