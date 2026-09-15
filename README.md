<div align="center">

<img src="assets/Engine Compagnion Logo.svg" width="110" alt="DJ Playlist Companion Logo">

# DJ Playlist Companion

**Die Schaltzentrale für deine Denon DJ / Engine DJ Musiksammlung**

Beta-Testversion für Windows 10 & 11 · Set-Arranger · 1-Klick-Aufräumen · Smart Track-Relocator

</div>

---

> ## ⚠️ Beta-Hinweis
> Diese Software ist eine **unfertige Testversion**. Sie verändert bei „Speichern"
> direkt deine Engine-DJ-Datenbank. **Lege vor dem Test ein Backup deiner
> Musikbibliothek an.** Nutzung auf eigenes Risiko – siehe
> [`BETA_TESTANLEITUNG.md`](BETA_TESTANLEITUNG.md).

## ⬇️ Download

**[➜ Aktuelle Beta herunterladen (GitHub Releases)](https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/download/v1.0.0-beta.2/DJ_Playlist_Companion_Demo_Setup.exe)**

| Datei | Beschreibung |
|---|---|
| `DJ_Playlist_Companion_Demo_Setup.exe` | Windows-Installer (empfohlen) – kein Administrator-Recht nötig |

Prüfsummen zur Kontrolle des Downloads: [`release/SHA256SUMS.txt`](release/SHA256SUMS.txt)

## ✨ Was kann das Programm?

| | Funktion | Beschreibung |
|---|---|---|
| <kbd>F8</kbd> | **Set-Arranger** | DJ-Sets mit automatischer Spannungsbogen-Optimierung („The Wave", „Progressive Ramp", „Peak-Time"), BPM- und Key-Flow-Analyse |
| <kbd>F3</kbd> | **Dubletten-Bereinigung** | Erkennt doppelte Titel und Tippfehler-Varianten, 1-Klick-Auto-Bereinigung |
| <kbd>F9</kbd> | **Genre-Manager** | Schreibweisen vereinheitlichen (z. B. `DnB` → `Drum & Bass`) |
| <kbd>F11</kbd> | **Artist-Manager** | A–Z-Schnellnavigation, Schreibweisen korrigieren (z. B. `tiesto` → `Tiësto`) |
| <kbd>F7</kbd> | **Smart Track-Relocator** | Fehlende oder verschobene Musikdateien automatisch wiederfinden und reparieren |
| <kbd>F6</kbd> | **Set-History** | Gespielte Gigs analysieren und als neue Playlist exportieren |
| <kbd>F10</kbd> | **CUE-Player** | Tracks vorhören (Leertaste = Play/Stop, Pfeiltasten = Spulen) |
| — | **Sicherheits-Backups** | Vor jeder dauerhaften Änderung wird automatisch eine Sicherung angelegt |

### Eindrücke

![Start](assets/screenshots/01-start.png)
![Set-Arranger](assets/screenshots/02-set-arranger.png)

Weitere Bilder: [Set-History](assets/screenshots/04-set-history.png) ·
[Track-Relocator](assets/screenshots/05-track-relocator.png) ·
[Genre-Manager](assets/screenshots/03-genre-manager.png) ·
[CUE-Player](assets/screenshots/06-cue-player.png)

## 🖥️ Systemvoraussetzungen

- **Windows 10 oder Windows 11 (64 Bit)**
- Eine **Engine-DJ-Bibliothek** (Engine DJ 3.x, 4.x & 5.0+) – auf dem PC oder
  auf einem USB-Stick / einer externen SSD
- Keine Python-Installation nötig: Die Anwendung ist ein eigenständiges
  Windows-Programm (Standalone, „Zero Dependency")

**Nicht** unterstützt: macOS/Linux, Pioneer rekordbox, Serato, Traktor.
Keine Verbindung zu inMusic Brands Inc. oder Denon DJ.

## 🚀 Installation

1. `DJ_Playlist_Companion_Demo_Setup.exe` aus den
   [Releases](https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/latest) herunterladen
2. Windows zeigt ggf. eine SmartScreen-Warnung (die Beta ist noch nicht
   signiert) → *Weitere Informationen* → *Trotzdem ausführen*
3. Setup durchklicken, optional Desktop-Verknüpfung aktivieren
4. Programm starten – beim ersten Start wird deine Engine-DJ-Bibliothek
   gesucht (`Engine Library/Database2/m.db`)

Ausführliche Anleitung inkl. Deinstallation: [`docs/INSTALLATION.md`](docs/INSTALLATION.md)

## 🧪 Beta testen & Feedback geben

Die genaue Testanleitung mit Checkliste steht in
[`BETA_TESTANLEITUNG.md`](BETA_TESTANLEITUNG.md).

- 🐞 **Fehler melden:** [Neues Issue anlegen](https://github.com/tintronik/DJ-Playlist-Companion-Beta/issues/new?template=bug_report.yml)
- 💬 **Fragen & Austausch:** [Discussions](https://github.com/tintronik/DJ-Playlist-Companion-Beta/discussions)

## 🔒 Datenschutz

- **Keine Telemetrie, kein Tracking, keine Nutzungsprofile.**
- Alle Daten bleiben lokal auf deinem Rechner
  (`%LOCALAPPDATA%\DJ Playlist Companion`).
- Die einzige Netzwerkverbindung entsteht nur dann, wenn du einen
  Pro-Lizenzschlüssel aktivierst (Lemon Squeezy).

Details: [`DATENSCHUTZ.md`](DATENSCHUTZ.md)

## ⏳ Testzeitraum

- Die Beta läuft **120 Tage lang ohne jede Einschränkung** – alle Funktionen,
  keine Track-Limits. Die Testzeit startet mit dem **ersten Programmstart**.
- Danach wechselt das Programm in den **Lese-Modus**: Sammlung ansehen, Sets
  planen, Audioanalyse und Backups bleiben möglich – **Speichern** in der
  Engine-DJ-Datenbank erst nach der Freischaltung. Es wird nichts gelöscht.
- Die Resttage siehst du jederzeit im Button **„Lizenz"** oben rechts.

## ⚠️ Bekannte Einschränkungen dieser Beta

- Eine **Pro-Version** ist in Vorbereitung. Der Kauf-Link im Lizenzdialog des
  Programms ist **noch nicht aktiv** und führt derzeit ins Leere – das ist
  bekannt und kein Fehler in deinem Setup.
- Die Beta ist **nicht digital signiert** → SmartScreen-Warnung beim Start.
- Änderungen werden nicht mit Engine DJ abgeglichen, solange Engine DJ geöffnet
  ist: Das Programm sollte bei laufendem Engine DJ **geschlossen** bleiben.
- Nur Windows 10/11 (64 Bit), nur Engine DJ.

## 📄 Lizenz

**Proprietär – alle Rechte vorbehalten.** Der Quellcode ist **nicht** Teil dieses
Repositories. Nutzung ausschließlich nach der Endnutzer-Lizenzvereinbarung:
siehe [`LICENSE.md`](LICENSE.md) und [`EULA.md`](EULA.md).

> *DJ Playlist Companion* ist eine unabhängige Software und steht in keiner
> geschäftlichen Verbindung zu inMusic Brands Inc. oder Denon DJ.
> **Engine DJ**, **Engine OS** und **Denon DJ** sind eingetragene Warenzeichen
> von inMusic Brands Inc.

---

<div align="center">
<sub>© 2026 Tintronik · DJ Playlist Companion · Alle Rechte vorbehalten</sub>
</div>
