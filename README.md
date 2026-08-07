<div align="center">

# Compile Studio (CS v4.2 Production)


### **A Zero-Latency, Browser-Native Web Development Environment**

[![License: MIT](https://img.shields.io/badge/License-MIT-007ACC.svg?style=for-the-badge)](#license)
[![Tailwind CSS](https://img.shields.io/badge/Styling-Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com)
[![CodeMirror 5](https://img.shields.io/badge/Editor-CodeMirror_5-3178C6?style=for-the-badge)](https://codemirror.net)
[![JSZip Integration](https://img.shields.io/badge/Export-JSZip-FFD43B?style=for-the-badge)](https://stuk.github.io/jszip/)

*Instant HTML5, CSS3, and JavaScript prototyping with zero server overhead and 100% client-side privacy.*

[Explore Features](#-feature-matrix) • [Architecture](#-system-architecture) • [Shortcuts](#-keyboard-shortcuts) • [Getting Started](#-getting-started)

---

</div>

## 📑 Table of Contents
- [Overview](#-overview)
- [Feature Matrix](#-feature-matrix)
- [System Architecture](#-system-architecture)
- [Deep Dive Specifications](#-deep-dive-specifications)
  - [Editor & Syntax Engine](#1-editor--syntax-engine)
  - [Virtual File System (VFS)](#2-virtual-file-system-vfs)
  - [Execution Sandbox & Viewport](#3-execution-sandbox--viewport)
  - [Console Drawer & REPL](#4-console-drawer--repl)
  - [Package Injector & Boilerplates](#5-package-injector--boilerplates)
- [Keyboard Shortcuts](#-keyboard-shortcuts)
- [Getting Started](#-getting-started)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌐 Overview

**Compile Studio Pro** is an open-source, client-side Integrated Development Environment (IDE) built specifically for rapid web application prototyping[cite: 1]. Operating entirely within the client's browser, it eliminates the need for node runtimes, heavy build chains, or backend servers[cite: 1].

It features an in-memory Virtual File System (VFS), an isolated `iframe` runtime sandbox, real-time error capturing, and instant `.zip` archiving—delivering a native desktop IDE experience inside a single web page[cite: 1].

---

## ⚡ Feature Matrix

| Feature | CodePen | JSFiddle | StackBlitz | **Compile Studio Pro** |
| :--- | :---: | :---: | :---: | :---: |
| **Offline Capability** | ❌ | ❌ | ⚠️ | **✅ 100% Client-Side**[cite: 1] |
| **Virtual File System** | ❌ | ❌ | ✅ | **✅ Native VFS**[cite: 1] |
| **Interactive Console REPL** | ⚠️ | ❌ | ✅ | **✅ Captured & Filtered**[cite: 1] |
| **Responsive Breakpoints** | ❌ | ❌ | ❌ | **✅ Built-in Viewport Controls**[cite: 1] |
| **Instant `.zip` Export** | ❌ | ❌ | ✅ | **✅ Client-Side JSZip**[cite: 1] |
| **Glassmorphism UI / Command Palette** | ❌ | ❌ | ❌ | **✅ Built-in (`Ctrl+K`)**[cite: 1] |

---

## 🏗️ System Architecture

┌────────────────────────────────────────────────────────────────────────┐
│                        COMPILE STUDIO PRO IDE                          │
├───────────────────┬───────────────────────────────┬────────────────────┤
│   FILE TREE / VFS │      CODEMIRROR 5 EDITOR      │ COMMAND PALETTE    │
│   (LocalStorage)  │   (Syntax, Folding, Beautify) │ (Ctrl + K)         │
└─────────┬─────────┴───────────────┬───────────────┴─────────┬──────────┘
│                         │                         │
▼                         ▼                         ▼
┌────────────────────────────────────────────────────────────────────────┐
│                      EXECUTION ENGINE (Sandbox)                        │
│                                                                        │
│   ┌────────────────────────────────────────────────────────────────┐   │
│   │                    Isolated  Container                  │   │
│   │   • Dynamic HTML/CSS Rendering                                 │   │
│   │   • JavaScript Execution Context                               │   │
│   │   • CDN Package Injection (React, Three.js, GSAP)              │   │
│   └───────────────────────────────┬────────────────────────────────┘   │
└───────────────────────────────────┼────────────────────────────────────┘
│ PostMessage Interceptor
▼
┌────────────────────────────────────────────────────────────────────────┐
│                       CONSOLE DRAWER & REPL                            │
│   • Log/Warn/Error Filtering   • Unhandled Exception Capture           │
│   • Dynamic JS Evaluator       • Interactive Output Window             │
└────────────────────────────────────────────────────────────────────────┘


---

## 🔬 Deep Dive Specifications

### 1. Editor & Syntax Engine
* **Engine**: Powered by CodeMirror 5 with Dracula and Neo visual themes[cite: 1].
* **Intelli-Tools**: Smart auto-closing tags and brackets, syntax highlighting, and code folding[cite: 1].
* **Code Quality**: One-touch automatic code formatting via `js-beautify` and persistent regex search/replace[cite: 1].

### 2. Virtual File System (VFS)
* **Persistence**: Synchronizes directly with browser `localStorage` for complete data retention[cite: 1].
* **Management**: Full file manipulation—create, rename, delete, and real-time search filtering[cite: 1].
* **Archiving**: Raw file import pipeline and instant single-click `.zip` bundle export using `JSZip`[cite: 1].

### 3. Execution Sandbox & Viewport
* **Security & Isolation**: Code runs within an isolated `iframe` sandbox to prevent scope leaks[cite: 1].
* **Responsive Emulation**: Instant preset toggles for Desktop, Tablet, and Mobile viewport sizes[cite: 1].
* **Display Utilities**: Variable zoom controls and Portrait/Landscape orientation swapping[cite: 1].

### 4. Console Drawer & REPL
* **Console Interceptor**: Captures `console.log`, `console.warn`, `console.error`, and `console.dir` calls[cite: 1].
* **Error Tracking**: Traps unhandled runtime errors and promise rejections directly from the sandbox[cite: 1].
* **Interactive REPL**: Live evaluation prompt with multi-level severity filtering[cite: 1].

### 5. Package Injector & Boilerplates
* **1-Click CDN Injection**: Instant dependency loading for Tailwind CSS, Bootstrap, React, Vue, Three.js, and GSAP[cite: 1].
* **Starter Templates**: Out-of-the-box setups for Glassmorphism UI, HTML5 Canvas 2D, Three.js 3D scenes, and React (via Babel)[cite: 1].

---

## 🎹 Keyboard Shortcuts

| Shortcut | Context | Action |
| :--- | :--- | :--- |
| `Ctrl + K` / `Cmd + K` | Global | Open Command Palette[cite: 1] |
| `Ctrl + Shift + F` | Editor | Auto-format current file via `js-beautify`[cite: 1] |
| `Ctrl + Shift + R` | Global | Force trigger sandbox re-compilation[cite: 1] |
| `Ctrl + \` | Global | Toggle Dark / Light visual theme[cite: 1] |

---

## 🚀 Getting Started

Since Compile Studio Pro is fully client-side, setup takes under 10 seconds[cite: 1].

### Direct Launch
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/compile-studio-pro.git](https://github.com/your-username/compile-studio-pro.git)
