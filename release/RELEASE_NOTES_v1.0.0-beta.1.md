# DJ Playlist Companion – v1.0.0-beta.1

**Erste öffentliche Beta-Version** für Windows 10 / 11 (64 Bit).

> ⚠️ **Beta:** unfertige Testversion. Bitte vor dem Test ein Backup der
> Engine-DJ-Bibliothek anlegen und Engine DJ beim Speichern geschlossen halten.

## ⬇️ Download

| Datei | Größe | Hinweis |
|---|---|---|
| `DJ_Playlist_Companion_Demo_Setup.exe` | 77,6 MB | Windows-Installer, **keine** Admin-Rechte nötig |

**SHA256:** `0F999BA589ADA389B29195B26F3056924CB6BED0F7E1309E527528AB4B681C98`

Prüfen mit:
```powershell
Get-FileHash -Algorithm SHA256 ".\DJ_Playlist_Companion_Demo_Setup.exe"
```

## ✨ Funktionen

- **Set-Arranger (F8):** Set-Vorbereitung mit Spannungsbogen-Optimierung
  („The Wave", „Progressive Ramp", „Peak-Time"), BPM- und Key-Flow
- **Dubletten-Bereinigung (F3):** doppelte Titel und Schreibweisen-Varianten
  finden und in einem Durchgang bereinigen
- **Genre-Manager (F9):** Genre-Schreibweisen vereinheitlichen
- **Artist-Manager (F11):** A–Z-Schnellnavigation und Korrektur von
  Schreibweisen
- **Smart Track-Relocator (F7):** verschobene Musikdateien wiederfinden und
  Verknüpfungen reparieren
- **Set-History (F6):** gespielte Gigs analysieren, als Playlist exportieren
- **CUE-Player (F10):** Tracks vorhören (Leertaste = Play/Stop)
- **Sicherheits-Backups:** automatische Sicherung vor dauerhaften Änderungen

## 🖥️ Voraussetzungen

- Windows 10 oder Windows 11 (64 Bit)
- Engine-DJ-Bibliothek (Engine DJ 3.x, 4.x & 5.0+), auf PC oder USB/SSD
- Keine Python-Installation, keine weiteren Abhängigkeiten

## ⚠️ Bekannte Einschränkungen

- **Demo-Limit:** maximal 5 Tracks bzw. 5 Gruppen pro Aktion.
  Eine Pro-Version ohne Limit ist in Vorbereitung.
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
