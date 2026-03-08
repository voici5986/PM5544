# PM5544 Canvas Editor

[English](./README.md) | [中文](./README.zh-CN.md)

A single-file HTML tool for previewing and exporting a PM5544-style card with configurable text bars.

---

## Overview

This project is a lightweight, zero-build editor for PM5544-style graphics.
Open `index.html` directly in a browser, edit text-bar parameters, preview instantly, and export:
- custom SVG
- self-contained HTML

---

## Why This Project

- Quickly generate PM5544-like visual cards with station/time/date overlays.
- Share reproducible results through URL query parameters.
- Export portable files (embedded assets, no external font/image dependency).

---

## Key Features

- Single-file app (`index.html`), no framework, no installation.
- Responsive preview canvas with 4:3 aspect ratio.
- Automatic `no signal` behavior below the minimum canvas threshold.
- Text bar controls:
- `tbar` (single top line)
- `tbar1` + `tbar2` (double top lines)
- `bbar` (bottom-left bar)
- `bbarfull` (bottom-center bar)
- Priority rule: `tbar` overrides `tbar1/tbar2`.
- Dynamic keywords:
- `TIME` for live clock
- `DATE` for live date
- Export options:
- SVG (embedded base plate + embedded font)
- HTML (self-contained file)

---

## Parameter Reference

| Param | Description |
|---|---|
| `tbar` | Large single top bar text |
| `tbar1` | Small top bar line 1 |
| `tbar2` | Small top bar line 2 |
| `bbar` | Bottom-left bar text |
| `bbarfull` | Bottom-center bar text |

Special tokens:
- `TIME` -> live time text
- `DATE` -> live date text

---

## Export Behavior

- **Exported HTML** is self-contained and keeps dynamic time/date updates.
- **Exported SVG** includes embedded assets and supports dynamic `TIME/DATE` via embedded script in script-enabled SVG viewers.
- In environments that block SVG script execution (for example, some image pipelines), dynamic text may appear as a static snapshot.

---

## Local Usage

1. Open `index.html` in a modern browser.
2. Fill any parameter fields.
3. Click:
- `应用并更新 URL` to sync current configuration into URL.
- `导出 SVG` or `导出 HTML` to export files.

---

## Project Files

- `index.html`: main app (UI, rendering, export logic, embedded assets)
- `colorrefer.png`, `PM5544_with_non-PAL_signals.png`: reference images

---

## Compatibility

Recommended browsers:
- Chrome (latest)
- Edge (latest)
- Firefox (latest)

No build pipeline is required.

---

## Note

This repository is intentionally kept as a single-page, single-file implementation for portability and easy sharing.

