# DocKit for Raycast

[中文](README.md) | **English**

Fix formatting in Word, PowerPoint, and Excel files — right from Raycast.

[![Raycast Store](https://img.shields.io/badge/Raycast_Store-pending-orange?style=for-the-badge)](https://www.raycast.com/zengtianli/dockit)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

## Install

> Raycast Store review is pending. Install from source for now:

1. Install the Python backend:
   ```bash
   pip install git+https://github.com/zengtianli/dockit.git
   ```

2. Install the extension:
   ```bash
   git clone https://github.com/zengtianli/dockit-raycast.git
   cd dockit-raycast
   npm install && npm run dev
   ```

3. Search for "Format Word" / "Convert Spreadsheet" / "Standardize PowerPoint" in Raycast to use the commands.

## Commands

| Command | Description |
|---------|------------|
| **Format Word Document** | Fix Chinese quote pairing, convert English punctuation to Chinese, standardize unit symbols (e.g. 平方米 → m²) |
| **Convert Spreadsheet Format** | Convert between Excel (XLSX), CSV, and TXT with auto-detection |
| **Standardize PowerPoint** | Unify fonts, fix text formatting, and set table styles in one click |

## How it works

```
Raycast (TypeScript) → subprocess → python3 -m dockit → dockit core
```

Select a file in Finder → trigger the command → see results in HUD toast → output file in the same directory.

## Prerequisites

- macOS
- Python 3.10+ with [dockit](https://github.com/zengtianli/dockit) installed
- Raycast

## Configuration

| Preference | Default | Description |
|-----------|---------|------------|
| Python Path | `/opt/homebrew/bin/python3` | Path to Python with dockit |

## Related

- [DocKit](https://github.com/zengtianli/dockit) — the Python core library
- [DocKit Web](https://dockit.tianli.cyou) — online demo, no install needed

## License

MIT
