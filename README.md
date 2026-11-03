# underground-local-music-player
made this project completely by myself The project’s code is Python, with a Windows batch script for building. Qt stylesheet/CSS-like rules are embedded in Python strings.


UNDERGROUND is a desktop music player for your own collection. It runs on Windows and keeps your library, playlists, and playback controls in one place.

## What it does

- Plays WAV, MP3, and OGG files.
- Imports individual tracks or scans a folder for music.
- Organizes tracks into playlists and a play queue.
- Supports shuffle, repeat, likes, and playback history.
- Reads track details and cover art from audio files, with options to edit them.
- Includes a Spotify link panel and optional track saving through `spotdl`.
- Lets you customize the theme, background, and other appearance settings.

Your imported audio is copied into the app's `music` folder; the originals are left where they are. Library details and preferences are saved locally.

## Run from source

Use Python 3.12 or 3.13, then install the project requirements:

powershell
python -m pip install -r requirements.txt
python main.py

 
You can also open `music\run_underground.pyw` to launch without a console window.

## Build for Windows

Run `BUILD_APP.bat`. It installs the build requirements and creates the packaged app in `dist\UNDERGROUND`.

## Notes

The Spotify panel uses Qt WebEngine, included with the project requirements. Saving tracks from Spotify links is optional and requires `spotdl`; it is not an official Spotify download feature. Only save music you have permission to download.

## Project files

- `main.py` — player interface, library, and playback
- `spotify.py` — Spotify panel and optional download integration
- `requirements.txt` — dependencies for running from source
- `requirements-build.txt` — dependencies for packaging
- `assets\` — app logo and icon
- `backgrounds\` — bundled background images
- `demo_music\` and `music\` — sample and local audio
