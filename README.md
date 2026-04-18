# 🖥️ NEXUS OS — Browser-Based Desktop Environment

> A fully-featured, production-grade Desktop OS simulation running entirely in the browser — built with React 18, Framer Motion, Zustand, and Tailwind CSS.

![React](https://img.shields.io/badge/React-18-61dafb?style=flat-square&logo=react)
![Framer Motion](https://img.shields.io/badge/Framer_Motion-11-ff69b4?style=flat-square)
![Zustand](https://img.shields.io/badge/Zustand-5-orange?style=flat-square)
![Vite](https://img.shields.io/badge/Vite-8-646cff?style=flat-square&logo=vite)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## ✨ Features

### 🪟 Window System
- **Draggable windows** — grab the titlebar and drag anywhere
- **Resizable from all 8 edges and corners**
- **Maximize / Minimize / Close** — macOS-style traffic light buttons
- **Window Snapping** — drag to screen edges to snap (Windows 11-style)
- **Multi-window management** — unlimited concurrent windows with z-index stacking
- **Spring animations** — powered by Framer Motion

### 🚀 Built-in Apps

| App | Description |
|-----|-------------|
| 📝 **Notes** | Rich note editor with sidebar, color labels, localStorage persistence |
| ⌨️ **Terminal** | Full bash simulator — ls, cd, cat, ping, neofetch, ps, top, tab-completion |
| 🖼️ **Gallery** | Image viewer with grid/list view, tag filters, lightbox with navigation |
| 🤖 **NEXUS AI** | Chat interface with intelligent mock responses, typing indicator |
| 📁 **Files** | Recursive tree file explorer with quick access sidebar |

### 🖥️ OS Shell
- Boot screen with animated progress bar
- App Launcher (Start Menu) with search and Settings tab
- Taskbar with dock, running window pills, clock, system tray
- 6 wallpapers + Dark/Light theme — both persistent
- Alt+Tab, Ctrl+Space, Ctrl+D keyboard shortcuts
- Toast notification system

---

## 📁 Folder Structure

```
nexus-os/
├── src/
│   ├── store/useOSStore.js           # Zustand — all OS state
│   ├── hooks/useKeyboardShortcuts.js
│   ├── components/
│   │   ├── desktop/
│   │   │   ├── Desktop.jsx
│   │   │   ├── AppLauncher.jsx
│   │   │   ├── BootScreen.jsx
│   │   │   └── SnapIndicator.jsx
│   │   ├── taskbar/Taskbar.jsx
│   │   ├── windows/
│   │   │   ├── WindowFrame.jsx      # Drag + resize engine
│   │   │   └── WindowManager.jsx    # Lazy-loaded app renderer
│   │   └── apps/
│   │       ├── notes/NotesApp.jsx
│   │       ├── terminal/TerminalApp.jsx
│   │       ├── gallery/GalleryApp.jsx
│   │       ├── ai/AIApp.jsx
│   │       └── files/FilesApp.jsx
│   ├── App.jsx
│   └── index.css
└── vite.config.js
```

---

## 🛠️ Getting Started

```bash
git clone https://github.com/GuGuMuGu/nexus-os.git
cd nexus-os
npm install
npm run dev
```

Open http://localhost:5173

### Build
```bash
npm run build
npm run preview
```

---

## 🚀 Deployment

### Vercel
```bash
npm i -g vercel && vercel --prod
```

### Netlify
Drag the `dist/` folder to [netlify.com/drop](https://app.netlify.com/drop)

Or add `netlify.toml`:
```toml
[build]
  publish = "dist"
  command = "npm run build"
```

### GitHub Pages
```bash
npm install --save-dev gh-pages
# Add to package.json scripts:
# "predeploy": "npm run build"
# "deploy": "gh-pages -d dist"
npm run deploy
```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Alt + Tab` | Cycle windows |
| `Ctrl + Space` | Toggle launcher |
| `Ctrl + D` | Show desktop (minimize all) |
| `Escape` | Close launcher |
| Double-click titlebar | Maximize/restore |
| Drag to screen edge | Snap window |

---

## 🧑‍💻 Built By

**Adarsh Sharma** — B.Tech ECE (ACT), Galgotias College
- Portfolio: [gugumugu.netlify.app](https://gugumugu.netlify.app)
- GitHub: [@GuGuMuGu](https://github.com/GuGuMuGu)

---

MIT License © 2025 Adarsh Sharma
