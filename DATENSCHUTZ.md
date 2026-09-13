# Datenschutz in der Beta-Version

**Kurzfassung: Es werden keine Daten an uns übertragen. Keine Telemetrie, kein
Tracking, keine Nutzungsstatistiken, keine Werbe-IDs.**

Stand: September 2026

---

## 1. Verantwortlicher

DJ Playlist Companion (Tintronik)
[VORNAME NACHNAME]
[STRASSE HAUSNUMMER]
[PLZ ORT]
Deutschland
E-Mail: [KONTAKT-E-MAIL]

> Die vollständigen Anbieterangaben werden mit Aufnahme des Verkaufs
> veröffentlicht. In der Beta-Phase ist der Support-Kanal auf GitHub erreichbar:
> <https://github.com/tintronik/DJ-Playlist-Companion-Beta/issues>

---

## 2. Welche Daten verarbeitet das Programm – und wo bleiben sie?

Das Programm läuft vollständig **lokal** auf deinem Rechner. Eine
Benutzeroberfläche wird als lokaler Server bereitgestellt und im
Anwendungsfenster angezeigt (`http://127.0.0.1`, nur auf dem eigenen Rechner
erreichbar – nicht aus dem Netzwerk).

Lokal gespeichert wird unter `%LOCALAPPDATA%\DJ Playlist Companion\`:

| Ordner/Datei | Inhalt |
|---|---|
| `config\settings.json` | von dir gewählte Datenbank, Backup-Ordner, Sprache |
| `temp\m.working.db` | Arbeitskopie deiner Engine-DJ-Datenbank (wird beim Speichern zurückgeschrieben) |
| `backups\` | automatische Sicherungen vor Änderungen |
| `cache\track_analysis.db` | berechnete Audio-Analysewerte (TrackDNA) |
| `logs\` | Protokolldateien des Programms |

Zusätzlich liest und schreibt das Programm – ausschließlich auf deine Anweisung –
deine **Engine-DJ-Datenbank** (`Engine Library\Database2\m.db`) an dem von dir
ausgewählten Ort (internes Laufwerk, USB-Stick oder externe SSD).

**Wir erhalten von diesen Daten nichts.** Es findet keine Übertragung an uns oder
an Dritte statt.

---

## 3. Netzwerkverbindungen

Das Programm baut **keine** Verbindung zu Servern von uns auf. Es gibt keine
Update-Prüfung und keine Absturzberichte.

Eine Ausnahme gibt es nur, wenn **du selbst** einen Pro-Lizenzschlüssel
aktivierst. Dann wird eine verschlüsselte Verbindung (HTTPS) zur Lizenz-API des
Zahlungsdienstleisters **Lemon Squeezy** aufgebaut:

- Endpunkt: `https://api.lemonsqueezy.com/v1/licenses/activate` (bzw.
  `.../deactivate`)
- Übertragen werden: der von dir eingegebene **Lizenzschlüssel** und ein
  **Instance-Name**. Dieser Instance-Name enthält einen kurzen
  **Maschinen-Kennwert** (SHA-256-Hash aus Windows-Computernamen und
  Benutzernamen, auf 16 Zeichen gekürzt), damit die Lizenz einem Gerät zugeordnet
  werden kann.
- Es werden **keine** Musikdaten, Dateipfade oder Bibliotheksinhalte übertragen.

Rechtsgrundlage für diese Verarbeitung ist die Vertragserfüllung
(Art. 6 Abs. 1 lit. b DSGVO). Weitere Informationen: <https://www.lemonsqueezy.com/privacy>

---

## 4. Browser

Die Oberfläche wird in einem eigenen Fenster von Microsoft Edge oder Google Chrome
(„App-Modus") angezeigt. Dabei werden **keine** externen Web-Inhalte, keine
Webfonts und keine Skripte Dritter geladen. Die Anzeige bleibt vollständig lokal.

---

## 5. Deine Rechte

Da wir keine personenbezogenen Daten von Beta-Testern erheben oder speichern,
können wir dazu keine Auskunft erteilen – es liegen schlicht keine Daten vor.

Wenn du im Rahmen eines Lizenzkaufs Daten bei Lemon Squeezy hinterlässt, gelten
deren Datenschutzbestimmungen. Bei Fragen zu dieser Erklärung erreichst du uns
über den oben genannten Kontakt.

---

## 6. Wichtig: Deine Backups

Das Programm verändert deine Engine-DJ-Datenbank. Lege vor dem Test – unabhängig
von den automatischen Backups des Programms – eine eigene Sicherung deiner
Musikbibliothek an. Das ist kein Datenschutzthema, aber die wichtigste
Vorsichtsmaßnahme beim Testen einer Beta-Version.
