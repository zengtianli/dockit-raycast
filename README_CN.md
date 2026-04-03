**中文** | [English](README.md)

# DocKit for Raycast

一键修复 Word、PowerPoint 和 Excel 文件的格式问题 — 直接在 Raycast 中操作。

[![Raycast Store](https://img.shields.io/badge/Raycast_Store-pending-orange?style=for-the-badge)](https://www.raycast.com/zengtianli/dockit)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

## 安装

> Raycast Store 审核中。目前通过源码安装：

```bash
# 安装 Python 后端
pip install git+https://github.com/zengtianli/dockit.git

# 安装扩展
git clone https://github.com/zengtianli/dockit-raycast.git
cd dockit-raycast
npm install && npm run dev
```

## 命令

| 命令 | 功能 |
|------|------|
| **Format Word Document** | 修复中文引号配对、英文标点转中文、标准化单位符号 |
| **Convert Spreadsheet Format** | Excel/CSV/TXT 格式转换，支持自动检测 |
| **Standardize PowerPoint** | 统一字体、修复文本格式、一键设置表格样式 |

## 工作原理

```
Raycast (TypeScript) → subprocess → python3 -m dockit → dockit core
```

Finder 选择文件 → 触发命令 → HUD 通知结果 → 输出保存到同一目录。

## 相关资源

- [DocKit](https://github.com/zengtianli/dockit) — Python 核心库
- [DocKit Web](https://dockit.tianlizeng.cloud) — 在线演示

## 许可证

MIT
