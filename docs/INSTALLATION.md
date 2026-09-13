# Installationsanleitung

## Voraussetzungen

| | |
|---|---|
| Betriebssystem | Windows 10 oder Windows 11, **64 Bit** |
| Engine DJ | Version 3.x, 4.x oder 5.0+ (Desktop oder USB/externe SSD) |
| Rechte | **Keine** Administratorrechte nötig |
| Zusätzliche Software | **Keine** – Python, .NET o. Ä. werden nicht benötigt |

> **Nicht unterstützt:** macOS, Linux, Pioneer rekordbox, Serato, Traktor.

## 1. Download

1. Öffne die Release-Seite:
   **https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/latest**
2. Lade unter *Assets* die Datei **`DJ_Playlist_Companion_Demo_Setup.exe`**
   herunter.
3. Optional: Prüfsumme vergleichen (`release/SHA256SUMS.txt`):

```powershell
Get-FileHash -Algorithm SHA256 ".\DJ_Playlist_Companion_Demo_Setup.exe"
```

## 2. SmartScreen-Warnung (normal in dieser Beta)

Die Beta ist **nicht digital signiert**. Windows zeigt daher möglicherweise
„Windows hat den Start dieses Programms verhindert" o. ä.

So startest du das Setup trotzdem:

1. Im Dialog auf **„Weitere Informationen"** klicken
2. Danach auf **„Trotzdem ausführen"**

Wenn dein Virenscanner die Datei blockiert, prüfe bitte zuerst die Prüfsumme und
melde den Fall gern als Issue – wir schauen es uns an.

## 3. Installation

1. `DJ_Playlist_Companion_Demo_Setup.exe` doppelklicken
2. Sprache wählen (Deutsch/Englisch)
3. Zielordner bestätigen (Standard: `%LOCALAPPDATA%\Programs\DJ Playlist Companion`)
4. Optional: **Desktop-Verknüpfung** aktivieren (*Aufgaben* → Häkchen setzen)
5. „Installieren" → das Programm startet direkt nach dem Setup

Das Setup legt außerdem einen Eintrag im **Startmenü** an.

## 4. Erster Start

1. Beim Start durchsucht das Programm deine Laufwerke nach der Datei
   `Engine Library\Database2\m.db`.
2. **Wird die Bibliothek nicht gefunden**, klicke oben auf *„Ordner wählen…"* und
   wähle den übergeordneten Ordner **`Engine Library`** aus.
3. Bei mehreren Bibliotheken (z. B. PC und USB-Stick) kannst du oben in der
   Kopfzeile oder im Einstellungsdialog (⚙) umschalten.
4. Prüfe die angezeigte Trackanzahl – sie sollte ungefähr mit Engine DJ
   übereinstimmen.

> ⚠️ **Vor der ersten Änderung:** Lege ein Backup deiner Engine-DJ-Bibliothek an
> und schließe Engine DJ, bevor du speicherst.

## 5. Wo liegen meine Daten?

| Ort | Inhalt |
|---|---|
| Installationsordner (`%LOCALAPPDATA%\Programs\DJ Playlist Companion`) | Programmdateien |
| `%LOCALAPPDATA%\DJ Playlist Companion\config` | Einstellungen |
| `%LOCALAPPDATA%\DJ Playlist Companion\temp` | Arbeitskopie der Datenbank |
| `%LOCALAPPDATA%\DJ Playlist Companion\backups` | automatische Backups |
| `%LOCALAPPDATA%\DJ Playlist Companion\logs` | Protokolldateien |

Deine **Musikdateien und die Original-Datenbank** bleiben dort, wo sie sind –
sie werden nur auf deine Anweisung verändert.

## 6. Update auf eine neuere Beta

1. Neue Setup-Datei aus den Releases herunterladen
2. Setup erneut ausführen – es ersetzt die Programmdateien
3. Deine Einstellungen und Backups unter `%LOCALAPPDATA%\DJ Playlist Companion\`
   bleiben erhalten

## 7. Deinstallation

**Variante A (empfohlen):** Windows-Einstellungen → *Apps* → *Installierte Apps* →
*DJ Playlist Companion* → *Deinstallieren*

**Variante B:** im Startmenü den Eintrag *Uninstall DJ Playlist Companion* wählen

Programmdateien werden dabei vollständig entfernt. Der Datenordner
`%LOCALAPPDATA%\DJ Playlist Companion\` mit Backups bleibt bewusst erhalten –
lösche ihn nur, wenn du sicher bist, dass du die Backups nicht mehr brauchst.

## 8. Probleme beim Start?

| Symptom | Ursache / Lösung |
|---|---|
| Fenster öffnet sich nicht | Edge oder Chrome muss vorhanden sein (in Windows 10/11 vorinstalliert). Alternativ öffnet sich der Standardbrowser. |
| „Bibliothek nicht gefunden" | Ordner `Engine Library` manuell auswählen; bei USB-Sticks sicherstellen, dass das Laufwerk eingebunden ist. |
| Änderungen kommen in Engine DJ nicht an | Engine DJ war beim Speichern geöffnet → schließen, erneut speichern. |
| Virenscanner meldet die Datei | Prüfsumme kontrollieren (Abschnitt 1) und Fall als Issue melden. |

Weitere Fragen: [`FAQ.md`](FAQ.md) ·
[Issues](https://github.com/tintronik/DJ-Playlist-Companion-Beta/issues)
