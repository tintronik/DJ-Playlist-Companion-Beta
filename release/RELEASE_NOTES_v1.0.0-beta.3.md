# DJ Playlist Companion – v1.0.0-beta.3

**Aktuelle Beta** für Windows 10 / 11 (64 Bit).

> ⏳ **Testzeitraum: 120 Tage voller Funktionsumfang** – alle Funktionen, keine
> Track-Limits. Danach wechselt das Programm in den Lese-Modus (Ansehen und
> Analysieren bleiben möglich, Speichern erst nach Freischaltung).
>
> ⚠️ Bitte vor dem Test ein **Backup der Engine-DJ-Bibliothek** anlegen und
> Engine DJ beim Speichern geschlossen halten.

## ⬇️ Download

| Datei | Größe | Hinweis |
|---|---|---|
| `DJ_Playlist_Companion_Demo_Setup.exe` | 89.053.116 Bytes (84,9 MB) | Windows-Installer, **keine** Admin-Rechte nötig |

**SHA256:** `26BB8B3622B739F555133CBA568298580BA968FD77E4FF786E5100D4D00214DF`

Prüfen mit:
```powershell
Get-FileHash -Algorithm SHA256 ".\DJ_Playlist_Companion_Demo_Setup.exe"
```

## 🆕 Neu in dieser Version

- **Neutrale Bezeichnung der Tonart-Spalte:** Die Spalte heißt in der
  Oberfläche jetzt **„Tonart"** (englisch: **„Key"**) und die Filterleiste
  **„Tonart wählen"**. Der Badge-Tooltip lautet **„Harmonische Tonart"**, der
  Sortierhinweis **„Standard: Tonart & BPM"**. Die angezeigten Werte (z. B. `8A`,
  `8B`) bleiben unverändert.
- Hintergrund: markenrechtliche Vorsicht – geschützte Fremdbezeichnungen werden
  im Programm, in den Downloads und in der Dokumentation nicht mehr verwendet.
- **Neue Screenshots** auf Basis einer vollständig synthetischen Demo-Bibliothek
  (keine echten Titel oder Artists).

## ✨ Funktionen

- **Set-Arranger (F8):** Set-Vorbereitung mit Spannungsbogen-Optimierung
  („The Wave", „Progressive Ramp", „Peak-Time"), BPM- und Tonart-Flow
- **Dubletten-Bereinigung (F3):** doppelte Titel und Schreibweisen-Varianten
  finden und in einem Durchgang bereinigen
- **Genre-Manager (F9):** Genre-Schreibweisen vereinheitlichen
- **Artist-Manager (F11):** A–Z-Schnellnavigation und Korrektur von Schreibweisen
- **Smart Track-Relocator (F7):** verschobene Musikdateien wiederfinden und
  Verknüpfungen reparieren
- **Set-History (F6):** gespielte Gigs analysieren, als Playlist exportieren
- **CUE-Player (F10):** Tracks vorhören (Leertaste = Play/Stop)
- **Sicherheits-Backups:** automatische Sicherung vor dauerhaften Änderungen

## ⏳ Testzeitraum im Detail

| | |
|---|---|
| Dauer in dieser Beta | **120 Tage** (Verkaufsversion später: 30 Tage) |
| Start | mit dem ersten Programmstart |
| Resttage sichtbar | Button **„Lizenz"** oben rechts in der Kopfzeile |
| Nach Ablauf | Lese-Modus – Ansicht, Planung, Analyse, Backups und Exporte bleiben frei |
| Gesperrt nach Ablauf | Schreiben in die Engine-DJ-Datenbank |

## 🖥️ Voraussetzungen

- Windows 10 oder Windows 11 (64 Bit)
- Engine-DJ-Bibliothek (Engine DJ 3.x, 4.x & 5.0+), auf PC oder USB/SSD
- Keine Python-Installation, keine weiteren Abhängigkeiten

## ⚠️ Bekannte Einschränkungen

- **Kauf-Link im Lizenzdialog ist noch nicht aktiv** – der Button führt derzeit
  ins Leere. Das ist bekannt und kein Installationsfehler.
- **Kein Code-Signing:** Windows zeigt beim Start ggf. eine
  SmartScreen-Warnung → *Weitere Informationen* → *Trotzdem ausführen*.
- Nur Windows und nur Engine DJ (kein rekordbox, Serato oder Traktor).

## 🔒 Datenschutz

Keine Telemetrie, kein Tracking. Alle Daten bleiben lokal
(`%LOCALAPPDATA%\DJ Playlist Companion`). Eine Netzwerkverbindung entsteht nur
bei der Aktivierung eines Pro-Lizenzschlüssels (Lemon Squeezy).

## 🐞 Feedback

- Fehler melden: [Bug-Report anlegen](../../issues/new?template=bug_report.yml)
- Fragen & Austausch: [Discussions](../../discussions)

Details zur Installation: [`docs/INSTALLATION.md`](../docs/INSTALLATION.md) ·
Häufige Fragen: [`docs/FAQ.md`](../docs/FAQ.md) ·
Testcheckliste: [`BETA_TESTANLEITUNG.md`](../BETA_TESTANLEITUNG.md)

---

*DJ Playlist Companion ist eine unabhängige Software und steht in keiner
geschäftlichen Verbindung zu inMusic Brands Inc. oder Denon DJ. Engine DJ,
Engine OS und Denon DJ sind eingetragene Warenzeichen von inMusic Brands Inc.*
