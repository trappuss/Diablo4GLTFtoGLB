[README.md](https://github.com/user-attachments/files/27572564/README.md)
# Diablo4GLTFtoGLB # 

Two tools for generating a `.glb` rigged version of models exported from **Diablo IV** with the tool [D4Analyzer](https://github.com/DiabloTools/Diablo4Tools-Releases). It can do this by pulling information from `.app.json` files found in [d4data(https://github.com/DiabloTools/d4data)] and translating it. This also means the tool exclusively functions based off of the informational available through [d4data(https://github.com/DiabloTools/d4data)]. Some models will still be encrypted and not have an available `.app.json` to pull from in-which I recommend waiting for another content update for Diablo 4 and trying again then.

![D4 Model Studio Screenshot](https://github.com/trappuss/Diablo4GLTFtoGLB/blob/main/preview.png?raw=true)

---

## Features

- **Batch conversion** — drag in a folder or use Grab Latest to auto-detect your most recent D4Analyzer export
- **Full armature** — bones, parent hierarchy, and skin weights (JOINTS_0 / WEIGHTS_0) are preserved
- **Texture embedding** — all materials and textures baked into a single self-contained `.glb`
- **Click **⟳ Grab Latest** to automatically find and load the most recently exported folder from D4Analyzer. No folder selection needed.**
- **Embedded 3D preview** — wireframe and shaded preview with skeleton overlay, directly in the app
- **Right-click export menu** — export to a custom folder, open in Explorer, and more

---

## Requirements

- Python 3.10+
- [D4Analyzer](https://github.com/DiabloTools/Diablo4Tools-Releases) (to export `.gltf` files from the game)

---

## Installation

- Download & Extract the latest [Release](https://github.com/trappuss/Diablo4GLTFtoGLB/releases)

---

## Usage

### GUI Version

Double-click `launch.bat` — it checks for Python, installs Pillow if needed, and starts the app.

Or run directly:

```bash
python Diablo4GLTFtoGLB.py
```

### Standalone Version

Drag & Drop a `.gltf` file exported from [D4Analyzer](https://github.com/DiabloTools/Diablo4Tools-Releases)  onto `d4_convert.py` and it'll generate a rigged `.glb` version next to it. You can also Drag & Drop a folder or multiple files for conversion as well.

---

## File Overview

| File | Description |
|------|-------------|
| `Diablo4GLTFtoGLB.py` | Main application (GUI + CLI) |
| `Diablo4GLTFtoGLB_standalone.py` | Standalone version with no gui, just drag and drop any .gltf file/s onto it and it'll generate a rigged .glb next to the .gltf files |
| `launch.bat` | Windows launcher with auto-install |
| `requirements.txt` | Python dependencies |

---

## To-Do List

- Standalone version should close automatically once finished.
- Standalone version should be able to drag and drop onto opened.
- GUI version should hide terminal.
- GUI version's 3d viewer doesn't show textures when textures are toggled.
- GUI version should be more compact.

---

## Links

- [Deviantart](https://www.deviantart.com/trappissy) Most of my model uploads are found here.
- [Patreon](https://www.patreon.com/TRAPPUSSY) Some of my archived mods are here, most of my stuff is free.
- [Ko-fi](https://ko-fi.com/trappucci) Donate here.

## Disclaimer

This tool is a fan project and is not affiliated with or endorsed by Blizzard Entertainment. Do not distribute Diablo IV game assets. Use extracted models for personal, non-commercial purposes only and in accordance with [Blizzard's Fan Art Policy](https://www.blizzard.com/en-us/legal/b9c9ed9e-ff4b-4bcd-b94e-2cfa02f69a7c/copyright-notices). Also this tool is made with AI so don't let anyone trick you into buying any tool similiar, it's just simple code. Actually don't buy anything, FUCK GATEKEEPING.
