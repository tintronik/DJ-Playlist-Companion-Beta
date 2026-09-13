# Häufige Fragen (FAQ)

## Allgemein

**Ist das Programm offiziell von Denon DJ / inMusic?**
Nein. *DJ Playlist Companion* ist eine unabhängige Software eines einzelnen
Entwicklers. Sie ist **nicht** mit inMusic Brands Inc., Denon DJ oder Engine DJ
verbunden oder von diesen freigegeben. „Engine DJ", „Engine OS" und „Denon DJ"
sind Warenzeichen von inMusic Brands Inc.

**Was kostet die Beta?**
Die Beta ist kostenlos. Die Testversion ist auf 5 Tracks bzw. 5 Gruppen pro
Aktion limitiert. Eine Pro-Version ohne Limit ist in Vorbereitung.

**Ich sehe im Lizenzdialog einen „Vollversion kaufen"-Button – wohin führt der?**
Noch ins Leere. Der Shop ist **noch nicht online**; das ist bekannt und kein
Fehler in deiner Installation. Sobald es Preise und einen Shop gibt, informieren
wir in den [Releases](https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases)
und in den [Discussions](https://github.com/tintronik/DJ-Playlist-Companion-Beta/discussions).

**Läuft das Programm auch auf macOS oder Linux?**
Aktuell nein – die Beta ist ausschließlich für Windows 10/11 (64 Bit).

**Funktioniert es mit Pioneer rekordbox, Serato oder Traktor?**
Nein. Das Programm arbeitet direkt mit der Engine-DJ-Datenbank
(`Engine Library\Database2\m.db`).

**Muss Engine DJ installiert sein?**
Nein. Es genügt, dass eine Engine-DJ-Bibliothek (Datenbank) vorhanden ist – auf
dem PC, einem USB-Stick oder einer externen SSD.

---

## Sicherheit und Daten

**Kann meine Musikbibliothek beschädigt werden?**
Das Programm legt vor dauerhaften Änderungen automatisch Sicherungen an
(`%LOCALAPPDATA%\DJ Playlist Companion\backups`). Trotzdem gilt: Für eine
Beta-Version solltest du **immer ein eigenes Backup** anlegen. Schreibe keine
Änderungen, solange **Engine DJ geöffnet** ist – das kann Dateien sperren.

**Werden meine Daten ins Internet übertragen?**
Nein. Es gibt keine Telemetrie und keinen Trackingdienst. Alles bleibt lokal.
Eine Netzwerkverbindung entsteht nur, wenn **du** einen Pro-Lizenzschlüssel
aktivierst (dann direkt zu Lemon Squeezy). Details: [`../DATENSCHUTZ.md`](../DATENSCHUTZ.md)

**Warum warnt Windows beim Start (SmartScreen)?**
Die Beta ist noch nicht digital signiert. Das ist normal für unfertige,
unveröffentlichte Builds. Du kannst die Datei über *Weitere Informationen* →
*Trotzdem ausführen* starten – vorher gern die Prüfsumme aus
[`../release/SHA256SUMS.txt`](../release/SHA256SUMS.txt) kontrollieren.

**Darf ich die Setup-Datei an Freunde weitergeben?**
Bitte nicht direkt weitergeben. Die Beta ist kostenlos, aber die Weitergabe der
Installationsdateien ist nach der EULA nicht gestattet. Verweise stattdessen auf
dieses Repository – so bekommt jeder die aktuelle Version und wir behalten den
Überblick über die Tester-Gruppe.

---

## Bedienung

**Meine Bibliothek wird nicht gefunden.**
Klicke im Datenbank-Auswahlfenster auf *„Ordner wählen…"* und wähle den Ordner
**`Engine Library`** aus. Bei externen Laufwerken prüfen, ob sie eingebunden sind.

**Ich nutze mehrere Bibliotheken (PC + USB-Stick).**
Du kannst oben in der Kopfzeile oder im Einstellungsdialog (⚙) umschalten.

**Änderungen erscheinen nicht in Engine DJ.**
Stelle sicher, dass Engine DJ vor dem Speichern **geschlossen** war, und lade die
Bibliothek in Engine DJ anschließend neu.

**Wo liegen die Protokolldateien?**
`%LOCALAPPDATA%\DJ Playlist Companion\logs` (`app.log`, `error.log`).
Bitte vor dem Hochladen in ein Issue auf persönliche Pfade prüfen.

**Wie deinstalliere ich die Beta?**
Windows-Einstellungen → *Apps* → *Installierte Apps* → *DJ Playlist Companion* →
*Deinstallieren*. Details: [`INSTALLATION.md`](INSTALLATION.md)

---

## Feedback

**Ich habe einen Fehler gefunden.**
➜ [Bug-Report anlegen](https://github.com/tintronik/DJ-Playlist-Companion-Beta/issues/new?template=bug_report.yml)

**Ich habe eine Idee oder eine Frage.**
➜ [Discussions](https://github.com/tintronik/DJ-Playlist-Companion-Beta/discussions)
