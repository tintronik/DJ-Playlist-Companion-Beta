# Beta-Testanleitung

Danke, dass du **DJ Playlist Companion** testest! Damit dein Feedback direkt
einfließen kann, findest du hier eine kurze Vorbereitung und eine Checkliste.

---

## 1. Vorbereitung (bitte nicht überspringen)

- [ ] **Backup deiner Engine-DJ-Bibliothek** anlegen (kompletter Ordner
      `Engine Library` auf dem jeweiligen Laufwerk).
- [ ] **Engine DJ schließen**, bevor du im Programm Änderungen speicherst –
      sonst können Dateien gesperrt sein.
- [ ] Prüfen, ob deine Bibliothek auf dem PC oder auf einem **USB-Stick /
      externen SSD** liegt. Beides ist zum Testen interessant.
- [ ] Notiere deine **Engine-DJ-Version** (3.x, 4.x, 5.x) und deine
      **Windows-Version**.

> 💡 **Tipp:** Wenn du zwei Bibliotheken hast, teste die Beta zuerst mit der
> weniger wichtigen.

## 2. Installation

Kurzanleitung: siehe [`../docs/INSTALLATION.md`](../docs/INSTALLATION.md).

Nach dem Start sollte sich das Anwendungsfenster öffnen und deine Bibliothek
automatisch gefunden werden. Falls nicht: oben rechts über das
Datenbank-Auswahlfenster den Ordner `Engine Library` manuell wählen.

---

## 3. Checkliste – diese Bereiche bitte durchtesten

Hake ab, was funktioniert hat, und melde alles, was nicht wie erwartet läuft.

### A) Start & Datenbank

- [ ] Programm startet ohne Fehlermeldung
- [ ] Bibliothek wird automatisch gefunden
- [ ] Wechsel zwischen zwei Bibliotheken (z. B. PC ↔ USB-Stick) funktioniert
- [ ] Trackanzahl in der Sammlung stimmt ungefähr mit Engine DJ überein
- [ ] Programm beendet sich sauber (keine „Geister"-Prozesse im Task-Manager)

### B) Set-Arranger (F8)

- [ ] Tracks in die Set-Vorbereitung ziehen (Drag & Drop)
- [ ] Eine Optimierung starten (z. B. „The Wave")
- [ ] Ergebnis ist nachvollziehbar (BPM-/Key-Verlauf wirkt sinnvoll)
- [ ] Set als Playlist in die Bibliothek zurückschreiben
- [ ] Set als `.m3u`-Datei exportieren

### C) Dubletten-Bereinigung (F3)

- [ ] Vorschlagsliste wird erzeugt
- [ ] Auswahl einzelner Gruppen möglich
- [ ] Ausführung + anschließende Kontrolle in Engine DJ

### D) Genre- und Artist-Manager (F9 / F11)

- [ ] Schreibweisen-Vorschläge sind sinnvoll (Umlaute, Groß-/Kleinschreibung)
- [ ] A–Z-Sprungleiste funktioniert
- [ ] Änderungen sind anschließend in Engine DJ sichtbar

### E) Smart Track-Relocator (F7)

- [ ] Verschobene Tracks werden erkannt
- [ ] Vorschläge für neue Pfade passen
- [ ] Reparatur funktioniert (Track ist danach abspielbar)

### F) Set-History (F6) & CUE-Player (F10)

- [ ] History-Sitzungen werden aufgelistet
- [ ] Export als Playlist funktioniert
- [ ] CUE-Player: Leertaste = Play/Stop, Pfeiltasten = Spulen

### G) Sicherheit & Backups

- [ ] Vor einer Änderung wurde ein Backup angelegt
      (`%LOCALAPPDATA%\DJ Playlist Companion\backups`)
- [ ] Ein Backup lässt sich wiederherstellen

---

## 4. Fehler melden

Am besten direkt als Issue mit dem vorbereiteten Formular:

**➜ https://github.com/tintronik/DJ-Playlist-Companion-Beta/issues/new?template=bug_report.yml**

Für allgemeine Fragen und Erfahrungsberichte:
**➜ https://github.com/tintronik/DJ-Playlist-Companion-Beta/discussions**

Hilfreich für uns:

| Angabe | Wo zu finden |
|---|---|
| Beta-Version | Dateiname der Setup-Datei (z. B. `v1.0.0-beta.3`) |
| Windows-Version | `winver` in der Windows-Suche |
| Engine-DJ-Version | Engine DJ → Info/Über |
| Schritte zum Nachstellen | 1, 2, 3 … so genau wie möglich |
| Fehlermeldung | möglichst wörtlich / als Screenshot |
| Logs | `%LOCALAPPDATA%\DJ Playlist Companion\logs` (`app.log`, `error.log`) |

> ⚠️ **Vor dem Hochladen prüfen:** Screenshots und Logs können **Dateipfade**
> (z. B. Musikordner) enthalten. Bitte unkenntlich machen, was nicht öffentlich
> sein soll – GitHub-Issues sind für jeden lesbar.

---

## 5. Was uns besonders hilft

- **Realistische Sets** – je größer/uneinheitlicher deine Bibliothek, desto
  wertvoller der Test.
- **Genauigkeit** – stimmen Titelanzahl, BPM- und Key-Werte mit Engine DJ überein?
- **Gefühl** – wirkt die Set-Reihenfolge musikalisch sinnvoll?
- **Grenzfälle** – Sonderzeichen, Umlaute, sehr lange Titel, fehlende Audio-Dateien.

Danke für deine Zeit! 🎧
