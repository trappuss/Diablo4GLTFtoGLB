[README.md](https://github.com/user-attachments/files/27572564/README.md)
# Diablo4GLTFtoGLB# D4 Model Studio

A GUI tool for converting **Diablo IV** model exports from [D4Analyzer](https://github.com/skarn/d4data) into fully-rigged `.glb` files ready for Blender, Unreal Engine, or any other 3D application.

![D4 Model Studio Screenshot](<img width="1102" height="772" alt="python_qzwl6WFbC3" src="https://github.com/user-attachments/assets/88f712dd-0b31-4dc7-83f2-8fd2619ff7d7" />
)

---

## Features

- **Batch conversion** — drag in a folder or use Grab Latest to auto-detect your most recent D4Analyzer export
- **Full armature** — bones, parent hierarchy, and skin weights (JOINTS_0 / WEIGHTS_0) are preserved
- **Texture embedding** — all materials and textures baked into a single self-contained `.glb`
- **Embedded 3D preview** — wireframe and shaded preview with skeleton overlay, directly in the app
- **Right-click export menu** — export to a custom folder, open in Explorer, and more
- **CLI mode** — run headless from the terminal for scripting and batch pipelines

---

## Requirements

- Python 3.10+
- [D4Analyzer](https://github.com/DiabloTools/Diablo4Tools-Releases![Uploading python_qzwl6WFbC3.png…]()
) (to export `.gltf` files from the game)

---

## Installation

```bash
git clone https://github.com/YOUR_USERNAME/d4-model-studio.git
cd d4-model-studio
pip install -r requirements.txt
```

---

## Usage

### GUI (recommended)

Double-click `launch.bat` — it checks for Python, installs Pillow if needed, and starts the app.

Or run directly:

```bash
python d4_model_studio.py
```

### Grab Latest

Click **⟳ Grab Latest** to automatically find and load the most recently exported folder from D4Analyzer. No folder selection needed.

### CLI

```bash
# Convert a single file
python d4_model_studio.py model.gltf

# Convert all .gltf files in a folder
python d4_model_studio.py --dir "C:\path\to\export" --output "C:\path\to\output"

# Convert without embedding textures
python d4_model_studio.py model.gltf --no-embed
```

---

## File Overview

| File | Description |
|------|-------------|
| `d4_model_studio.py` | Main application (GUI + CLI) |
| `d4_convert.py` | Standalone conversion engine |
| `launch.bat` | Windows launcher with auto-install |
| `requirements.txt` | Python dependencies |

---

## Disclaimer

This tool is a fan project and is not affiliated with or endorsed by Blizzard Entertainment. Do not distribute Diablo IV game assets. Use extracted models for personal, non-commercial purposes only and in accordance with [Blizzard's Fan Art Policy](https://www.blizzard.com/en-us/legal/b9c9ed9e-ff4b-4bcd-b94e-2cfa02f69a7c/copyright-notices).
