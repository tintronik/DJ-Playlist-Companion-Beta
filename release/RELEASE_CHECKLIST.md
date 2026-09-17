# Release-Checkliste (Beta)

Kurzablauf fuer jede neue Beta-Version. Ziel: **genau ein** Release, das GitHub als
„Latest" fuehrt, und **kein** alter Download, der noch erreichbar ist.

Stand: 17.09.2026 (`v1.0.0-beta.3` veroeffentlicht, `v1.0.0-beta.2` entfernt).

---

## 0. Voraussetzungen (einmalig pruefen)

| Punkt | Soll-Zustand |
|---|---|
| Sichtbarkeit des Beta-Repos | **Public** – bei privatem Repo sind Release-Downloads fuer Aussenstehende nicht abrufbar |
| Landingpage | Repo `djplaylist.github.io`, Branch `main` (GitHub Pages) |
| `gh` CLI | nicht erforderlich, die Web-Oberflaeche reicht |
| Build-Werkzeuge | Python 3 + PyInstaller, Inno Setup 6 (`ISCC.exe`) |

---

## 1. Build erzeugen (Quellcode-Repo)

```powershell
cd "D:\Dokumente\GitHub\DJ-Playlist-Companion-Privat"
python build_releases.py
```

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

- [ ] `release/RELEASE_NOTES_v<version>.md` anlegen
- [ ] `release/SHA256SUMS.txt`: neue Version als „aktuell", Vorgaenger als „ersetzt" eintragen
- [ ] `CHANGELOG.md`: neuen Abschnitt oben ergaenzen
- [ ] `README.md`: beide Download-Buttons auf die neue Asset-URL umstellen
      (`/releases/download/v<version>/DJ_Playlist_Companion_Demo_Setup.exe`)
- [ ] Committen und nach `main` pushen

---

## 3. Release veroeffentlichen

GitHub → Repo `DJ-Playlist-Companion-Beta` → **Releases → Draft a new release**

- [ ] Tag: `v<version>` neu anlegen lassen, Target `main`
- [ ] Titel: `DJ Playlist Companion v<version>`
- [ ] Asset: `DJ_Playlist_Companion_Demo_Setup.exe` hochladen
      (optional zusaetzlich `DJ_Playlist_Companion_Demo_Windows.zip`)
- [ ] Beschreibung aus `release/RELEASE_NOTES_v<version>.md` einfuegen
- [ ] **„Set as the latest release" aktiv**
- [ ] **„Set as a pre-release" NICHT aktiv**

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
