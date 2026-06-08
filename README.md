# Stadtteilzentren Berlin – Websitedaten

Dieses Repository enthält die aktuellen Exportdateien der geförderten Stadtteilzentren, Nachbarschaftshäuser, Selbsthilfekontaktstellen und verwandter Einrichtungen in Berlin, die über das [Infrastrukturförderprogramm Stadtteilzentren](https://www.berlin.de/sen/soziales/buergerschaftliches-engagement/stadtteilzentren/) der Senatsverwaltung für Soziales gefördert werden.

## Inhalt

| Datei | Beschreibung |
|---|---|
| `STZ_Website.csv` | Aktuelle Exportliste aller Stadtteilzentren und Nachbarschaftstreffs mit Status „In Betrieb" |
| `SHK_Website.csv` | Aktuelle Exportliste aller Selbsthilfekontaktstellen |

## Datenquelle

Die Daten werden aus einer SQLite-Datenbank exportiert und bei Bedarf aktualisiert. `STZ_Website.csv` enthält nur Einrichtungen, die zum Zeitpunkt des Exports aktiv „In Betrieb" sind. Einrichtungen mit dem Typ „MOST-Ausgangsstandort" und „Selbsthilfekontaktstelle" sind dort nicht enthalten – letztere sind in `SHK_Website.csv` separat erfasst.

## Spalten STZ_Website.csv

| Spalte | Beschreibung |
|---|---|
| `Standortnummer` | Eindeutige Projekt-ID des Standorts |
| `Einrichtungsname` | Name der Einrichtung |
| `Einrichtungsart` | Typ (z. B. Stadtteilzentrum, Nachbarschaftstreff) |
| `Adresse` | Straße und Hausnummer |
| `PLZ` | Postleitzahl |
| `Stadt` | Stadt |
| `Bezirk` | Berliner Verwaltungsbezirk |
| `Webseite` | URL der Einrichtung |
| `Telefon` | Telefonnummer |
| `E_Mail` | E-Mail-Adresse |
| `Angebot` | Angebotsbeschreibung |
| `Träger` | Name des Trägers |
| `Anmerkungen` | Weitere Anmerkungen |
| `Kurzbeschreibung` | Beschreibungstext der Einrichtung |
| `X_Koordinate` | Geografische Länge (Longitude) |
| `Y_Koordinate` | Geografische Breite (Latitude) |
| `Foto_Link` | Link zu einem Foto der Einrichtung |
| `Google_Maps_Link` | Link zur Google Maps Position |
| `Sachstand` | Datum der letzten Änderung |

## Spalten SHK_Website.csv

| Spalte | Beschreibung |
|---|---|
| `Geschäftskennzeichen` | Eindeutige Projekt-ID des Standorts |
| `Einrichtungsname` | Name der Einrichtung |
| `Einrichtungsart` | Typ (Selbsthilfekontaktstelle) |
| `Adresse` | Straße und Hausnummer |
| `PLZ` | Postleitzahl |
| `Stadt` | Stadt |
| `Bezirk` | Berliner Verwaltungsbezirk |
| `Webseite` | URL der Einrichtung |
| `Telefon` | Telefonnummer |
| `E_Mail` | E-Mail-Adresse |
| `Träger` | Name des Trägers |
| `Google_Maps_Link` | Link zur Google Maps Position |
| `Sachstand` | Datum der letzten Änderung |

## Format

- Trennzeichen: `,` (Komma)
- Zeichenkodierung: UTF-8
- Zeilenenden: Unix (LF)
- Erste Zeile: Spaltenüberschriften

## Nutzung

Die Rohdateien sind direkt abrufbar unter:

```
https://raw.githubusercontent.com/ifpstz/website-data/main/STZ.csv
https://raw.githubusercontent.com/ifpstz/website-data/main/SHK.csv
```

## Aktualisierung

Die Dateien werden nach inhaltlichen Änderungen in der Quelldatenbank manuell aktualisiert. Die Versionshistorie der Commits zeigt, welche Einrichtungen sich zwischen zwei Exporten geändert haben.
