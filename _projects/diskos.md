---
layout: project
title: "DiskOS V1.8"
tech_stack: "[Vanilla JS] [HTML5 Canvas] [Web Audio API]"
demo_link: "http://www.diskos.net" 
github_link: "http://github.com/p1e85/DiskOS"
image: "/assets/img/diskos.png"
---

A fully functional, browser-based retro operating system and 8-bit game engine built entirely in vanilla web technologies. 

Designed to seamlessly bridge desktop keyboard input and mobile touchscreen interfaces, it boots directly into a classic CRT terminal environment.

### The Proprietary Virtual File System (VFS)
DiskOS manages an internal file structure using HTML5 LocalStorage, driven by custom file extensions:

* **.diskCODE:** The core programming language. A custom BASIC-style syntax that handles logic (IF/THEN, GOTO), memory manipulation (PEEK/POKE), variables, audio synthesis (BEEP/PLAY), and drawing to a 64x32 grid.
* **.diskGUI:** A hybrid CSS-injector and menu generator. It allows raw scripts to instantly alter global OS colors, typography, CRT scanlines, and generate interactive menus.
* **.diskPAD:** A mobile controller compiler. Scripts can spawn custom on-screen Gamepads that automatically map to keyboard logic.
* **.diskROM:** The "Cartridge" format. A master file that packages code, themes, and gamepads together, allowing users to EXPORT to a physical file and IMPORT via drag-and-drop.
* **.diskDIR:** Virtual directory sandboxing to keep projects organized in memory.

### Core Technical Architecture
* **Renderer:** Custom 60FPS Canvas API render loop drawing a rigid 64x32 cell grid.
* **Audio:** Native Web Audio API implementation for synthesizing square-wave frequencies and raw musical notes.
* **Mobile Tech:** Employs a hidden "Ghost Textarea" script to hijack native mobile keyboards, allowing true command-line typing on iOS and Android without breaking the canvas viewport.