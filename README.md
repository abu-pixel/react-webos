# AETHER OS

> A complete desktop environment that lives inside a single HTML file.

AETHER OS is a ground-up redesign of this project: a glassy, animated, local-first browser operating system built with React 18. It keeps the zero-build-step architecture of the original, so the exact same file runs from your file system and from Vercel.

![AETHER OS](https://img.shields.io/badge/AETHER%20OS-4.0.0-8b5cf6?style=for-the-badge)
![React](https://img.shields.io/badge/React-18-22d3ee?style=for-the-badge)
![Build](https://img.shields.io/badge/build-none-a3e635?style=for-the-badge)
![Storage](https://img.shields.io/badge/storage-localStorage-fb7185?style=for-the-badge)

## What changed

The previous "Super Extreme" desktop was replaced with an entirely new system:

- New identity, visual language, icon set, wallpapers, animations, and window chrome.
- Boot sequence, lock screen, command palette, quick settings, notification center, and desktop context menu.
- Eight-direction window resizing, edge snapping, maximize/restore, minimize, focus management, and a live dock.
- A real file model with folders, favorites, trash/restore, sorting, search, import/export, and backups.
- Ten full applications instead of the original four.
- Legacy workspaces are detected and upgraded automatically on first load.

## Applications

| App | What it does |
| --- | --- |
| **Explorer** | File manager with sidebar locations, breadcrumbs, grid/list views, sorting, search, inline creation, rename, star, trash, restore, and downloads. |
| **Terminal** | `aether-sh` with history (up/down arrows), tab completion, and commands including `help`, `ls`, `cat`, `touch`, `mkdir`, `rm`, `mv`, `star`, `find`, `open`, `theme`, `wall`, `echo`, `date`, `whoami`, `clear`, `history`, `neofetch`, and `export`. |
| **Code Editor** | Line numbers, tab insertion, word wrap, adjustable font size, caret position, line/character count, dirty state, save, and download. |
| **Paint Studio** | Brush, eraser, line, rectangle, ellipse, color palette, custom color, brush size, undo/redo, clear, and save to Files as PNG. |
| **Gallery** | Image library with previews, lightbox navigation, and downloads. |
| **Notes** | Multiple colored notes with titles, auto-save, and trash support. |
| **Calculator** | Mouse and keyboard input with a sanitized expression evaluator. |
| **System Monitor** | Animated CPU/memory/network graphs, process list, and session statistics. |
| **Settings** | Themes, accent colors, wallpapers, custom wallpaper URL, animation/glass/icon toggles, brightness, JSON backup/restore, and system reset. |
| **About** | System information and build details. |

## Shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl/Cmd + K` | Toggle the command palette (apps, files, actions) |
| `Ctrl/Cmd + N` | Create and open a new text file in the editor |
| `Ctrl/Cmd + S` | Save the active editor file |
| `Ctrl/Cmd + W` | Close the top window |
| `Alt + Tab` | Cycle to the next window |
| `Esc` | Close the palette or the top window |
| Double-click title bar | Maximize / restore |
| Drag to screen edge | Snap window left / right / top |
| Right-click desktop | Quick actions menu |
| Drag files onto desktop | Import them into Files |

## Themes and wallpapers

Three themes: **Dark**, **Light**, and **Eclipse**. Six accent colors and five procedural wallpapers (nebula, aurora, sunset, ocean, mono), plus custom image URLs. Everything is applied instantly from Settings, Quick Settings, the desktop menu, or the Terminal (`theme` and `wall` commands).

## Storage and persistence

All files, notes, settings, window geometry, favorites, and desktop icon positions are saved in `localStorage` under `aether-os-v4`. Nothing is uploaded anywhere. Settings includes JSON backup export/import so a workspace can be moved between browsers.

If a workspace from the older **React WebOS - Super Extreme** build is found in `localStorage`, AETHER OS upgrades it on first boot and shows a welcome notification.

## Installation / usage

### Run locally

1. Clone or download this repository.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).
3. No install, bundler, or dev server is required.

Optional: serve the folder with VS Code Live Server or any static HTTP server.

### Vercel

This repository is a static site: `index.html` sits at the root and there is no build step. A push to `main` triggers the existing Vercel deployment, and the deployed link serves the same file you see locally. No `package.json`, framework preset, or environment variables are needed.

To verify a deployment, open the Vercel URL and check that the boot screen says **AETHER OS** and the top bar shows the AETHER mark.

## Technical details

- React 18 (UMD) and ReactDOM 18 loaded from unpkg.
- Babel Standalone compiles the JSX directly in the browser.
- Vanilla CSS for the entire desktop shell, window manager, and applications.
- `localStorage` for all persistent state.
- One file, no dependencies to install, no server-side code.

## Repository

`github.com/abu-pixel/react-webos`
