# DJ Playlist Companion – v1.0.0-beta.6

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
| `DJ_Playlist_Companion_Demo_Setup.exe` | 114,489,778 bytes (109.2 MB) | Windows installer, **no** administrator rights required |

**SHA256:** `4832E4B805CFDE1162967B3A6FAFDDA7E98D07AB1A5E10D6340AD0D421D019C8`

Verify your download with:

```powershell
Get-FileHash -Algorithm SHA256 ".\DJ_Playlist_Companion_Demo_Setup.exe"
```

## 🆕 New in this version

- **Smart Match & similarity panel (new):** the **Match** button now opens a right-hand
  slide-over panel that combines all three match dimensions in one place: harmonic key,
  BPM tolerance (± 4 %) and a new **acoustic Klang-Match** (100-dimensional texture
  vector computed from your MP3s). Preview any hit directly and drag it into your set
  or add it with **+ Set** – fully local, no cloud, no subscription.
- **New panel filters:** genre, character, minimum rating, BPM tolerance and
  “not already in this set”.
- **Background indexing:** your library is embedded in the background with a live
  progress read-out – the match list fills in while you keep working.
- **TrackDNA V2 character scoring in AutoFill:** the Set-Arranger Auto-Fill now also
  weighs *how a track sounds* (five-dimension character label) next to *where it
  historically played*. Active by default (weights 0.10/0.10), can be switched off
  via `use_dna_v2=False`.
- **More accurate audio vectors:** MP3 frame-based offset detection; DNA caches
  invalidate automatically when a file changes.
- **Database hygiene:** SQLite sidecar files are cleaned up automatically and stale
  history orphans are kept out of the Engine database; backup cleanup now sorts by age.
- **Set-Arranger header wraps** instead of clipping its buttons in narrow windows.
- This build reports the internal build ID `20261106-beta6`, which matches the release.

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
