# DJ Playlist Companion – v1.0.0-beta.4

**Current beta** for Windows 10 / 11 (64-bit).

> ⏳ **Test period: 120 days with the full feature set** – every tool unlocked, no track
> limits. After that the app switches to read-only mode (viewing, set planning, audio
> analysis and backups stay available; saving requires activation). Nothing is deleted.
>
> ⚠️ Please **back up your Engine DJ library** before testing and keep **Engine DJ closed**
> while DJ Playlist Companion writes to the database.

## ⬇️ Download

| File | Size | Note |
|---|---|---|
| `DJ_Playlist_Companion_Demo_Setup.exe` | 89,067,750 bytes (84.9 MB) | Windows installer, **no** administrator rights required |

**SHA256:** `2A3761F8A2383E46E50F05FF4B7604DBD0F070C46E59FA44789D2DE3A53AADEF`

Verify your download with:

```powershell
Get-FileHash -Algorithm SHA256 ".\DJ_Playlist_Companion_Demo_Setup.exe"
```

## 🆕 New in this version

- **Star rating directly in the collection:** every track can now be rated and re-rated
  from the collection view – no detour through a detail dialog. The rating is written to
  the Engine DJ database as usual, with the automatic backup running before the change.
- **Show and hide columns:** the columns of the **collection** and of the
  **Set-Arranger** can now be hidden, and the original layout comes back with one click
  (*Restore default*). The menu opens from the column button in the toolbar or with a
  right click on the column header.
- The column selection is **stored permanently** and survives a restart. Hidden columns
  are display-only: filtering, sorting and facet counting stay untouched – and the
  `Title` column cannot be hidden.
- **Note for bug reports:** this build reports the internal build ID `20260917-beta3`.
  That ID belongs to the beta.4 build – please still quote `1.0.0-beta.4` in your reports.

## ✨ Features

- **Set-Arranger (F8):** set preparation with tension-curve optimisation (The Wave,
  Progressive Ramp, Peak-Time), BPM and key flow
- **Duplicate Cleaner (F3):** find duplicate titles and spelling variants and clean them
  up in one pass
- **Genre Manager (F9):** unify genre spellings
- **Artist Manager (F11):** A–Z quick navigation and correction of spellings
- **Smart Track Relocator (F7):** find moved audio files and repair the library entries
- **Set History (F6):** analyse played gigs and export them as a playlist
- **CUE Player (F10):** preview tracks (Space = play/stop)
- **Safety backups:** automatic backup before every permanent change

## ⏳ Test period in detail

| | |
|---|---|
| Duration in this beta | **120 days** (sales version later: 30 days) |
| Start | with the first launch |
| Remaining days | licence button in the top-right corner |
| After expiry | read-only mode – viewing, planning, analysis, backups and exports stay free |
| Blocked after expiry | writing to the Engine DJ database |

## 🖥️ Requirements

- Windows 10 or Windows 11 (64-bit)
- An Engine DJ library (Engine DJ 3.x, 4.x & 5.0+), on a PC, USB stick or external SSD
- No Python installation and no other dependencies

## ⚠️ Known limitations

- **The purchase link in the licence dialog is not active yet** – the button currently
  leads nowhere. This is known and not an installation error.
- **No code signing:** Windows may show a SmartScreen warning → *More info* →
  *Run anyway*.
- Windows and Engine DJ only (no rekordbox, Serato or Traktor).

## 🔒 Privacy

No telemetry, no tracking. All data stays local
(`%LOCALAPPDATA%\DJ Playlist Companion`). A network connection is only opened when you
activate a Pro licence key (Lemon Squeezy).

## 🐞 Feedback

- Report a bug: [bug report template](https://github.com/tintronik/DJ-Playlist-Companion-Beta/issues/new?template=bug_report.yml)
- Questions & exchange: [Discussions](https://github.com/tintronik/DJ-Playlist-Companion-Beta/discussions)

Documentation: [Installation guide](https://github.com/tintronik/DJ-Playlist-Companion-Beta/blob/main/docs/INSTALLATION.md) ·
[FAQ](https://github.com/tintronik/DJ-Playlist-Companion-Beta/blob/main/docs/FAQ.md) ·
[Beta test checklist (German)](https://github.com/tintronik/DJ-Playlist-Companion-Beta/blob/main/BETA_TESTANLEITUNG.md) ·
[Checksums](https://github.com/tintronik/DJ-Playlist-Companion-Beta/blob/main/release/SHA256SUMS.txt)

---

*DJ Playlist Companion is an independent software project and is not affiliated with
inMusic Brands Inc. or Denon DJ. Engine DJ, Engine OS and Denon DJ are registered
trademarks of inMusic Brands Inc.*
