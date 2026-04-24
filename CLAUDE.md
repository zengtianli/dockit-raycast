# dockit-raycast — Raycast 扩展，修复 Word/PPT/Excel 格式问题

## Quick Reference

| 项目 | 路径/值 |
|------|---------|
| 扩展根目录 | `/Users/tianli/Dev/tools/raycast/dockit-ext/` |
| 命令入口 | `src/format-word.tsx` / `src/convert-format.tsx` / `src/standardize-ppt.tsx` |
| Python 后端 | `python3 -m dockit`（需安装 dockit 包） |
| Python 路径 | `/opt/homebrew/bin/python3` |
| 调用链 | Raycast (TypeScript) → subprocess → `python3 -m dockit` |
| 在线 Demo | https://dockit.tianlizeng.cloud |

## 常用命令

```bash
# 开发模式（在 Raycast 中热重载）
cd /Users/tianli/Dev/tools/raycast/dockit-ext
npm run dev

# 构建
npm run build

# Lint
npm run lint

# 更新 dockit Python 核心
pip install --upgrade git+https://github.com/zengtianli/dockit.git
```

## 项目结构

```
src/
├── format-word.tsx       # Format Word Document 命令
├── convert-format.tsx    # Convert Spreadsheet Format 命令
├── standardize-ppt.tsx   # Standardize PowerPoint 命令
└── utils/                # 公共工具函数
```

## 命令功能速查

| 命令 | 功能 |
|------|------|
| Format Word Document | 中文引号配对、英文标点转中文、单位符号标准化（m²等） |
| Convert Spreadsheet Format | XLSX / CSV / TXT 互转，自动识别格式 |
| Standardize PowerPoint | 统一字体、修复文本格式、设置表格样式 |

## 开发注意事项

- 扩展为 `no-view` 模式，结果通过 HUD toast 展示
- 输出文件与输入文件同目录
- Python 路径可在 Raycast Preferences 中修改，默认 `/opt/homebrew/bin/python3`
- 修改 `src/` 下 tsx 文件后，`npm run dev` 状态下 Raycast 自动热重载
- 发布前需通过 `npm run build` + `npm run lint` 无报错
