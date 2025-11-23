# LRCLIB Lyrics External Save (Picard Plugin)

This MusicBrainz Picard plugin fetches lyrics from **LRCLIB** after files are saved,
and writes them as **external sidecar files**:

- Synced lyrics → `*.lrc`
- Plain lyrics → `*.txt`

Sidecar files are saved **in the same folder** and with the **same base filename**
as the audio file.

The plugin **does not modify audio tags** and does not embed lyrics into files.

---

## 🚀 Features

✔ Fetch synced (`syncedLyrics`) or plain (`plainLyrics`) lyrics
✔ Write `.lrc` or `.txt` sidecar files
✔ Works after renaming / moving files
✔ Pure post-save logic → no crashes, no metadata conflicts
✔ Compatible with macOS (SSL verification disabled to avoid certificate issues)
✔ No modification to embedded tags

---

## 🧩 Installation

1. Download the latest release ZIP.
2. In Picard, open: `Options → Plugins → Install plugin…`
3. Select the ZIP file.
4. Enable “**LRCLIB Lyrics External Save**”.

---

## 🛠 How it Works

1. You save files in Picard.
2. Picard writes and moves files to their final location.
3. This plugin:

- Reads metadata (`title`, `artist`, `album`, `~length`)
- Queries `https://lrclib.net/api/get`
- Writes `.lrc` or `.txt` beside the audio file

---

## 📄 License

MIT License
Copyright (c)
