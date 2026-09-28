# Release-Checkliste (Beta)

Kurzablauf fuer jede neue Beta-Version. Ziel: **genau ein** Release, das GitHub als
„Latest" fuehrt, und **kein** alter Download, der noch erreichbar ist.

Stand: 28.09.2026 (`v1.0.0-beta.4` veroeffentlicht, `v1.0.0-beta.3` entfernt).

> Die Landingpage (`djplaylist.github.io`) verlinkt bewusst **`/releases/latest`** und
> nennt keine Versionsnummer – solange genau ein Release existiert und dieses **nicht**
> als Pre-release markiert ist, zeigt sie nach jeder neuen Beta automatisch die richtige
> Datei. Feste Versionslinks muessen dann nirgends gepflegt werden.

---

## 0. Voraussetzungen (einmalig pruefen)

| Punkt | Soll-Zustand |
|---|---|
| Sichtbarkeit des Beta-Repos | **Public** – bei privatem Repo sind Release-Downloads fuer Aussenstehende nicht abrufbar |
| Landingpage | Repo `djplaylist.github.io`, Branch `main` (GitHub Pages) |
| `gh` CLI | optional – die Web-Oberflaeche reicht ebenfalls. Installiert unter `C:\Program Files\GitHub CLI\gh.exe` (v2.101.0); fuer die Nutzung einmalig `gh auth login` |
| Build-Werkzeuge | Python 3 + PyInstaller, Inno Setup 6 (`ISCC.exe`) |

---

## 1. Build erzeugen (Quellcode-Repo)

```powershell
cd "D:\Dokumente\GitHub\DJ-Playlist-Companion-Privat"
python build_releases.py
```

> **Vor dem Build die Build-Kennung bumpen.** In
> `01_DJ_Playlist_Companion_Pro\backend\version.py` **und** in der Kopie
> `02_Commercial_Edition\backend\version.py` steht `VERSION_BUILD` (z. B.
> `"20260917-beta3"`). Diese Kennung liefert die App ueber `/version` aus; laeuft sie
> der Release-Nummer hinterher, melden Tester die falsche Version.
> Beispiel: fuer `v1.0.0-beta.5` → `VERSION_BUILD = "20260928-beta5"`.

Ergebnis:

- `03_Installer_Releases\DJ_Playlist_Companion_Demo_Setup.exe`
- zusaetzliche Kopie in `04_Website_und_Marketing\downloads\`

Groesse und Pruefsumme notieren (beide gehoeren in die Doku):

```powershell
Get-Item "03_Installer_Releases\DJ_Playlist_Companion_Demo_Setup.exe" | Select-Object Length, LastWriteTime
Get-FileHash -Algorithm SHA256 "03_Installer_Releases\DJ_Playlist_Companion_Demo_Setup.exe" | Format-List
```

---

## 2. Dokumentation aktualisieren (Beta-Repo)

- [ ] `release/RELEASE_NOTES_v<version>.md` anlegen (Vorlage: die Datei der Vorgaengerversion)
- [ ] `release/SHA256SUMS.txt`: neue Version als „aktuell", Vorgaenger als „ersetzt" eintragen
- [ ] `CHANGELOG.md`: neuen Abschnitt oben ergaenzen, beim Vorgaenger „aktuelle Beta" entfernen
- [ ] `README.md`: Versionslabel (`Latest beta`, Download-Button-Text) aktualisieren.
      Die Links zeigen bewusst auf **`/releases/latest`** – dann ist pro Release keine
      Asset-URL zu pflegen
- [ ] `BETA_TESTANLEITUNG.md`: Beispiel-Version in der Tabelle „Fehler melden" pruefen
- [ ] Committen und nach `main` pushen

---

## 3. Release veroeffentlichen

GitHub → Repo `DJ-Playlist-Companion-Beta` → **Releases → Draft a new release**

- [ ] Tag: `v<version>` neu anlegen lassen, Target `main`
- [ ] Titel: `DJ Playlist Companion v<version>`
- [ ] Asset: `DJ_Playlist_Companion_Demo_Setup.exe` hochladen
      (optional zusaetzlich `DJ_Playlist_Companion_Demo_Windows.zip`)
- [ ] Beschreibung aus `release/RELEASE_NOTES_v<version>.md` einfuegen
      (Links darin als **absolute URLs** – relative `../../`-Pfade laufen im Release ins Leere)
- [ ] **„Set as the latest release" aktiv**
- [ ] **„Set as a pre-release" NICHT aktiv**

### Schneller Weg: dieselben Schritte per `gh` CLI

Setzt Titel, Beschreibung, Assets und „latest" in einem Durchlauf (Voraussetzung:
`gh auth login` wurde einmalig ausgefuehrt):

```powershell
$V = "v1.0.0-beta.5"                                        # Zielversion
$R = "tintronik/DJ-Playlist-Companion-Beta"
$SRC = "D:\Dokumente\GitHub\DJ-Playlist-Companion-Privat\03_Installer_Releases\DJ_Playlist_Companion_Demo_Setup.exe"
$DOC = "D:\Dokumente\GitHub\DJ-Playlist-Companion-Beta\release"

# Release anlegen (laedt Installer + Release-Text hoch, setzt „latest")
gh release create $V $SRC --repo $R `
  --title "DJ Playlist Companion $V" --notes-file "$DOC\RELEASE_NOTES_$V.md" --latest

# Pruefsummen zusaetzlich als Asset
gh release upload $V "$DOC\SHA256SUMS.txt" --repo $R --clobber

# Bestehendes Release korrigieren (Text, Titel, latest):
gh release edit $V --repo $R --title "DJ Playlist Companion $V" `
  --notes-file "$DOC\RELEASE_NOTES_$V.md" --latest --prerelease=false
```

> Ein Release, das als *Pre-release* veroeffentlicht wird, zaehlt nicht als „latest".
> Gibt es nur Pre-Releases, antwortet
> `…/releases/latest` mit **404** – und damit laufen die Download-Buttons der
> Landingpage ins Leere.

---

## 4. Alte Version entfernen

- [ ] Altes Release loeschen (Releases → Version → *Delete*)
- [ ] Alten **Tag** zusaetzlich loeschen – das Loeschen des Releases entfernt den Tag nicht:

```powershell
cd "D:\Dokumente\GitHub\DJ-Playlist-Companion-Beta"
git push origin --delete v<alte-version>
git tag -d v<alte-version>
git ls-remote --tags origin      # Gegenprobe: nur die aktuelle Version darf uebrig sein
```

---

## 5. Gegenprobe – ohne Anmeldung

```powershell
# 1) muss 200 liefern und auf /releases/tag/v<version> enden
curl.exe -s -o NUL -w "%{http_code} %{url_effective}`n" -L https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/latest

# 2) neues Asset muss 206 (oder 200) liefern
curl.exe -s -o NUL -w "%{http_code}`n" -r 0-0 -L https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/download/v<version>/DJ_Playlist_Companion_Demo_Setup.exe

# 3) alte Version muss 404 liefern
curl.exe -s -o NUL -w "%{http_code}`n" -L https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/download/v<alte-version>/DJ_Playlist_Companion_Demo_Setup.exe

# 4) Downloads ueber /releases/latest/... (genau der Weg der Landingpage)
curl.exe -s -o NUL -w "%{http_code}`n" -L https://github.com/tintronik/DJ-Playlist-Companion-Beta/releases/latest/download/DJ_Playlist_Companion_Demo_Setup.exe
```

Zusaetzlich per `gh` (falls angemeldet):

```powershell
gh api repos/tintronik/DJ-Playlist-Companion-Beta/releases/latest --jq .tag_name   # muss v<version> sein
gh release view v<version> --repo tintronik/DJ-Playlist-Companion-Beta --json name,isPrerelease,isDraft,assets
gh release download v<version> --repo tintronik/DJ-Playlist-Companion-Beta --pattern SHA256SUMS.txt --dir $env:TEMP\ghchk --clobber
Get-FileHash "$env:TEMP\ghchk\SHA256SUMS.txt"    # muss dem lokalen release\SHA256SUMS.txt entsprechen
```

- [ ] Landingpage im **Inkognito-Fenster** oeffnen und einen Download-Button klicken
      (https://tintronik.github.io/djplaylist.github.io/) – die Buttons folgen
      automatisch `/releases/latest`, die Seite muss nicht geaendert werden
- [ ] Groesse und SHA256 des Downloads mit `release/SHA256SUMS.txt` vergleichen
- [ ] Ausgeloggt pruefen: nur so faellt auf, wenn das Repo (wieder) privat ist

---

## 6. Wenn `/releases/latest` 404 liefert

| Ursache | Loesung |
|---|---|
| Repo ist privat | Settings → General → Danger Zone → *Change repository visibility* → **Public** |
| Nur Pre-Releases vorhanden | neues Release als regulaeres Release veroeffentlichen (Pre-Release-Haken entfernen) |
| Alle Releases geloescht | mindestens ein veroeffentlichtes Release behalten |

---

## 7. Bekannte Stolperfallen aus dem beta.3-Release

- Der Installer liegt im **Quellcode-Repo** (`DJ-Playlist-Companion-Privat\03_Installer_Releases`),
  nicht im Beta-Repo – dort sind `*.exe` per `.gitignore` ausgeschlossen.
- Der `_backup`-Ordner enthaelt gleichnamige Setups aelterer Builds:
  fuer den Upload immer die Datei direkt im `03_Installer_Releases`-Ordner verwenden
  (Groesse und SHA256 gegen `release/SHA256SUMS.txt` pruefen).
- Release-Downloads immer ausgeloggt testen.
- `gh auth login` verlangt beim Einlesen eines Tokens die Scopes `repo` **und**
  `read:org`. Das im Windows-Anmeldeinformationsspeicher hinterlegte Git-Token von
  Git Credential Manager hat `read:org` nicht und wird deshalb abgelehnt
  (`error validating token: missing required scope 'read:org'`). Deshalb entweder
  `gh auth login` **interaktiv im Browser** ausfuehren oder einen Token mit beiden
  Scopes erzeugen (`gh auth login --with-token`).
