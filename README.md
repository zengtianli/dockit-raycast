# DocKit for Raycast

Fix formatting in Word, PowerPoint, and Excel files — right from Raycast.

[![Raycast Store](https://img.shields.io/badge/Raycast_Store-pending-orange?style=for-the-badge)](https://www.raycast.com/zengtianli/dockit)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

## Install

> Raycast Store 审核中。目前通过源码安装：

1. 安装 Python 后端：
   ```bash
   pip install git+https://github.com/zengtianli/dockit.git
   ```

2. 安装扩展：
   ```bash
   git clone https://github.com/zengtianli/dockit-raycast.git
   cd dockit-raycast
   npm install && npm run dev
   ```

3. 在 Raycast 中搜索 "Format Word" / "Convert Spreadsheet" / "Standardize PowerPoint" 即可使用

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
| Python Path | `/Users/tianli/miniforge3/bin/python3` | Path to Python with dockit |

## Related

- [DocKit](https://github.com/zengtianli/dockit) — the Python core library
- [DocKit Web](https://dockit.tianlizeng.cloud) — online demo, no install needed

## License

MIT
