# NINTENDO: Nintendo Quest (inoffizielles internes Lernprojekt)

**Datei:** `index.html` (eine Datei, offline lauffähig, Version 1.3.1, Stand 14.10.2026). Einfach im Browser öffnen oder auf einem Webserver ablegen.

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

Spielmechanik: 10 Münzen je richtiger Antwort, 1 bis 3 Sterne je Lektion (50 %, 75 %, 100 %), 5 Ränge von "Pilz-Praktikant" bis "Legende", Konfetti bei bestandenem Level, Fortschritt im Browser gespeichert (`localStorage`), Hell- und Dunkelmodus, Tastaturbedienung, "weniger Bewegung" wird beachtet.

## Veröffentlichung und Link-Vorschau
Geplante Adresse: https://nosz.github.io/nintendo/ (GitHub Pages, Repository `nintendo`, Dateien `index.html` und `nintendo_vorschau.jpg` ins Hauptverzeichnis legen). Die Vorschau (Open Graph / Twitter Card) zeigt `nintendo_vorschau.jpg` (1200 x 630, bunte Spielkarten, Sterne, Münze) mit Titel und Beschreibung. Wichtig: Die Bild-Adresse in den Tags ist absolut und gilt nur unter dieser Adresse; Messenger und Netzwerke speichern Vorschauen zwischen (nach dem Hochladen ggf. mit dem Debugger der jeweiligen Plattform neu einlesen). Vor einer öffentlichen Freigabe Management/Legal einbeziehen (siehe Grenzen).

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
- 1.3.1 (14.10.2026): Überschriftenebene in Lektionen korrigiert (h2), leerer Fortschritt bei 0 richtig vermieden; Link-Vorschau (Open Graph, Twitter Card), Vorschaubild, Favicon; Datei in index.html umbenannt.
- 1.3.0 (14.10.2026): Lektion 1 und 2 auf je 2 Karten und 2 Fragen gekürzt, Erfolg bei der ersten richtigen Antwort, Zertifikat direkt auf der Ergebnisseite, goldene Sterne im Ergebnis.
