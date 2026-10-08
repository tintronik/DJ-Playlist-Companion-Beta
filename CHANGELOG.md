# Änderungsverlauf

Alle nennenswerten Änderungen an den veröffentlichten Beta-Versionen.

## [v1.0.0-beta.5] – aktuelle Beta

**Drag and Drop für Genre Pflege**

- Jeder Track lässt sich jetzt im Genre Bereich auf ein Genre Label ziehen. 
- Der Auto-Fill des Set-Arrangers kann die Bewertung weiterhin als Filter nutzen.

**Markierung von Tracks im Set-Arranger**

- Es lassen sich mehrere Tracks mittels Shift-Taste + Klick im **Set-Arrangers** markieren und auch fixieren oder entfernen
  **„Standard wiederherstellen"** bringt das Ursprungslayout mit einem Klick zurück.
- Die Optimierung der Tracklist zeigt durch optimiertes Feedback ihren Bearbeitungsstand

## [v1.0.0-beta.4] – vorherige Beta

**Bewertung (Sterne) direkt in der Sammlung**

- Jeder Track lässt sich jetzt **direkt in der Sammlung** mit Sternen bewerten und
  umbewerten – ohne Umweg über einen Detaildialog. Die Bewertung wird wie gewohnt in die
  Engine-DJ-Datenbank geschrieben, das automatische Backup greift vorher.
- Der Auto-Fill des Set-Arrangers kann die Bewertung weiterhin als Filter nutzen.

**Spalten ein- und ausblenden**

- Die Spalten der **Sammlung** und des **Set-Arrangers** lassen sich jetzt ausblenden;
  **„Standard wiederherstellen"** bringt das Ursprungslayout mit einem Klick zurück.
  Das Menü öffnet der Spalten-Button in der Toolbar bzw. ein Rechtsklick auf den
  Spaltenkopf.
- Die Auswahl ist **dauerhaft gespeichert** und übersteht einen Neustart; ältere Layouts
  werden automatisch übernommen und bleiben vollständig sichtbar.
- Ausgeblendete Spalten sind reine Anzeige: **Filterkette, Sortierung und
  Facetten-Zählung bleiben unverändert**, und die Spalte „Titel" lässt sich nicht
  ausblenden.

## [v1.0.0-beta.3] – vorherige Beta

**Neutrale Bezeichnung für die Tonart-Spalte**

- Die Tonart-Spalte heißt in der Oberfläche jetzt **„Tonart"** (englisch: **„Key"**)
  und die Filterleiste dazu **„Tonart wählen"**. Die angezeigten Werte (z. B. `8A`,
  `8B`) bleiben unverändert.
- Der Badge-Tooltip lautet jetzt **„Harmonische Tonart: …"**, der Sortierhinweis
  **„Standard: Tonart & BPM"**.
- Hintergrund: markenrechtliche Vorsicht – geschützte Fremdbezeichnungen werden im
  Programm, in den Downloads und in der Dokumentation nicht mehr verwendet.

**Neue Screenshots**

- Alle Bilder wurden mit einer vollständig synthetischen Demo-Bibliothek neu
  aufgenommen (keine echten Titel, Artists oder Cover).

## [v1.0.0-beta.2] – erste veröffentlichte Beta

**Neu: Testzeitraum statt Demo-Limit**

- Die Begrenzung auf 5 Tracks bzw. 5 Gruppen ist **entfallen**.
- Die Beta läuft **120 Tage lang ohne jede Einschränkung** (in der späteren
  Verkaufsversion sind es 30 Tage ab dem ersten Start).
- Nach Ablauf wechselt das Programm in den **Lese-Modus**: Sammlung ansehen,
  Sets planen, Audioanalyse und Backups bleiben möglich – **Speichern** in der
  Engine-DJ-Datenbank erst nach der Freischaltung. Es wird nichts gelöscht.
- Die Sperre wird **im Backend** durchgesetzt, nicht mehr nur in der Oberfläche.
- Lizenzanzeige zeigt „✓ PRO AKTIV", „⏳ TESTVERSION – noch N Tage" oder
  „⚠️ TESTZEIT ABGELAUFEN"; abgelaufene Schreibversuche öffnen den Lizenzdialog.
- Splash-Screen: Titel jetzt „DJ Playlist Companion" (vorher „ENGINE Playlist
  COMPANION") und neutraler Begrüßungstext.

## [v1.0.0-beta.1] – nicht veröffentlicht

Interne Vorabversion; durch beta.2 ersetzt (enthielt noch das 5-Track-Limit).

**Enthaltene Funktionen**

- **Set-Arranger (F8):** Set-Vorbereitung mit Spannungsbogen-Optimierung
  („The Wave", „Progressive Ramp", „Peak-Time"), BPM- und Key-Flow-Analyse
- **Dubletten-Bereinigung (F3):** Erkennung doppelter Titel und
  Schreibweisen-Varianten, 1-Klick-Auto-Bereinigung
- **Genre-Manager (F9):** Vereinheitlichung von Genre-Schreibweisen
- **Artist-Manager (F11):** A–Z-Schnellnavigation und Korrektur von
  Schreibweisen
- **Smart Track-Relocator (F7):** Wiederfinden und Reparieren verschobener
  Musikdateien
- **Set-History (F6):** Analyse gespielter Gigs und Export als Playlist
- **CUE-Player (F10):** Vorhören von Tracks (Leertaste = Play/Stop)
- **Sicherheits-Backups:** automatische Sicherung vor dauerhaften Änderungen

**Bekannte Einschränkungen**

- Demo-Limit: maximal 5 Tracks bzw. 5 Gruppen pro Aktion (in beta.2 entfallen)
- Der Kauf-Link im Lizenzdialog ist noch nicht aktiv
- Kein Code-Signing – Windows SmartScreen warnt beim Start
- Nur Windows 10/11 (64 Bit), nur Engine DJ

**Datenschutz**

- Keine Telemetrie; alle Daten bleiben lokal (siehe `DATENSCHUTZ.md`)

---

## Geplant für die nächsten Beta-Versionen

- Rückmeldungen aus der Beta-Phase einarbeiten
- Verbesserungen an Analyse- und Sortierqualität
- Aufbau der Bezugsseite für die Vollversion
