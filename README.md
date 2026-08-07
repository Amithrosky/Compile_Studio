<div align="center">

# Compile Studio (CS v5.0 Production)


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

**Compile Studio Pro** is an open-source, client-side Integrated Development Environment (IDE) built specifically for rapid web application prototyping. Operating entirely within the client's browser, it eliminates the need for node runtimes, heavy build chains, or backend servers.

It features an in-memory Virtual File System (VFS), an isolated `iframe` runtime sandbox, real-time error capturing, and instant `.zip` archiving—delivering a native desktop IDE experience inside a single web page.

---

## ⚡ Feature Matrix

| Feature | CodePen | JSFiddle | StackBlitz | **Compile Studio Pro** |
| :--- | :---: | :---: | :---: | :---: |
| **Offline Capability** | ❌ | ❌ | ⚠️ | **✅ 100% Client-Side**  |
| **Virtual File System** | ❌ | ❌ | ✅ | **✅ Native VFS**  |
| **Interactive Console REPL** | ⚠️ | ❌ | ✅ | **✅ Captured & Filtered**  |
| **Responsive Breakpoints** | ❌ | ❌ | ❌ | **✅ Built-in Viewport Controls**  |
| **Instant `.zip` Export** | ❌ | ❌ | ✅ | **✅ Client-Side JSZip**  |
| **Glassmorphism UI / Command Palette** | ❌ | ❌ | ❌ | **✅ Built-in (`Ctrl+K`)**  |

---

## 🏗️ System Architecture

* **Vacant**

---

## 🔬 Deep Dive Specifications

### 1. Editor & Syntax Engine
* **Engine**: Powered by CodeMirror 5 with Dracula and Neo visual themes.
* **Intelli-Tools**: Smart auto-closing tags and brackets, syntax highlighting, and code folding.
* **Code Quality**: One-touch automatic code formatting via `js-beautify` and persistent regex search/replace.

### 2. Virtual File System (VFS)
* **Persistence**: Synchronizes directly with browser `localStorage` for complete data retention.
* **Management**: Full file manipulation—create, rename, delete, and real-time search filtering.
* **Archiving**: Raw file import pipeline and instant single-click `.zip` bundle export using `JSZip`.

### 3. Execution Sandbox & Viewport
* **Security & Isolation**: Code runs within an isolated `iframe` sandbox to prevent scope leaks.
* **Responsive Emulation**: Instant preset toggles for Desktop, Tablet, and Mobile viewport sizes.
* **Display Utilities**: Variable zoom controls and Portrait/Landscape orientation swapping.

### 4. Console Drawer & REPL
* **Console Interceptor**: Captures `console.log`, `console.warn`, `console.error`, and `console.dir` calls.
* **Error Tracking**: Traps unhandled runtime errors and promise rejections directly from the sandbox.
* **Interactive REPL**: Live evaluation prompt with multi-level severity filtering.

### 5. Package Injector & Boilerplates
* **1-Click CDN Injection**: Instant dependency loading for Tailwind CSS, Bootstrap, React, Vue, Three.js, and GSAP.
* **Starter Templates**: Out-of-the-box setups for Glassmorphism UI, HTML5 Canvas 2D, Three.js 3D scenes, and React (via Babel).

---

## 🎹 Keyboard Shortcuts

| Shortcut | Context | Action |
| :--- | :--- | :--- |
| `Ctrl + K` / `Cmd + K` | Global | Open Command Palette  |
| `Ctrl + Shift + F` | Editor | Auto-format current file via `js-beautify`  |
| `Ctrl + Shift + R` | Global | Force trigger sandbox re-compilation  |
| `Ctrl + \` | Global | Toggle Dark / Light visual theme  |

---

## 🚀 Getting Started

Since Compile Studio Pro is fully client-side, setup takes under 10 seconds.

### Direct Launch
1. Open the link:
```bash
# (https://amithrosky.github.io/Compile_Studio/?)
  
