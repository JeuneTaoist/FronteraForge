[![Download](https://img.shields.io/github/v/release/JeuneTaoist/FronteraForge?label=Download&color=7c5cfc&style=for-the-badge)](https://github.com/JeuneTaoist/FronteraForge/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/JeuneTaoist/FronteraForge/total?color=34d399&style=for-the-badge)](https://github.com/JeuneTaoist/FronteraForge/releases)

# FronteraForge

### [⬇️ Download the latest version](https://github.com/JeuneTaoist/FronteraForge/releases/latest)

**The all-in-one desktop translation studio for manhwa & manga.**

FronteraForge lets you translate manhwa/manga chapters with professional-quality text styling, AI-powered inpainting, and a seamless vertical reading workflow — all from a single desktop app. No internet required, everything runs locally on your machine.

> 🇫🇷 Français | 🇬🇧 English | 🇪🇸 Español — Interface auto-detected from your system language

---

## Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Detailed Guide](#detailed-guide)
- [Features](#features)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [FAQ](#faq)
- [Terms of Use](#terms-of-use)
- [Support](#support)

---

## Installation

### Windows (64-bit)

1. Download `FronteraForge_x.x.x_x64-setup.exe` from the [Releases](../../releases) page
2. Run the installer
3. **Read and accept the Terms of Use** (required to use the app)
4. Launch FronteraForge from your desktop or Start menu

### Requirements

- Windows 10 or 11 (64-bit)
- ~500MB disk space (includes AI models for OCR and inpainting)
- No internet connection required after installation

---

## Quick Start

| Step | What to do |
|------|-----------|
| **1** | Click **"Open"** and select a folder containing your manhwa chapter images (numbered: 1.jpg, 2.jpg, ...) |
| **2** | Use the **pencil tool** ✏ to draw zones around text, or click **"Launch OCR"** for automatic detection |
| **3** | Type your translations in the **left panel**, choose your text style and inpainting mode |
| **4** | Click **"Export"** — a `_trad` folder is created next to your original folder with all translated pages |

---

## Detailed Guide

### Step 1 — Import a chapter

Click the **"Open"** button (or press `Ctrl+O`) and select a folder containing your manhwa/manga images.

**Important:**
- Images should be **numbered** (1.jpg, 2.jpg, ... or 001.png, 002.png, ...)
- Supported formats: **JPG, PNG, WebP, BMP, TIFF**
- Images are displayed in **vertical scroll** mode, like reading on a phone
- The app will automatically look for a previous save file (`.manhwatl.json`) in the folder

### Step 2 — Detect text

You have **two methods** to detect text:

#### Method A — Automatic OCR (all pages)
1. Click **"Launch OCR"** in the top bar
2. A confirmation dialog will warn you that this may take time
3. Click **"Launch OCR"** to confirm
4. Wait for the progress bar to complete — the app will detect all text bubbles automatically
5. Detected bubbles appear with purple overlays on the images and cards in the left panel

#### Method B — Manual selection (pencil tool)
1. Click **"✏ Pencil"** in the top bar (or press `Ctrl+D`)
2. Choose a shape in the bottom bar: **Rectangle**, **Ellipse**, or **Diamond**
3. Click and drag on the image to draw a zone around text
4. The zone is added as a bubble in the left panel
5. Click **"Detect (N)"** to run OCR only on your manually drawn zones

**Tip:** Method B is faster and more precise for manhwa with complex layouts. Use Method A for standard manga with clear speech bubbles.

### Step 3 — Translate and style

Each detected bubble appears as a **card** in the left panel:

#### Translation
- The **original text** (detected by OCR) is shown in dark background
- Type your **translation** in the text field below
- Click **"Confirm"** when you're satisfied with the translation

#### Inpainting mode (how the original text is removed)
Choose from the dropdown in each bubble card:

| Mode | Description | Best for |
|------|------------|----------|
| **Bubble** | Fills with the median background color | White/solid color speech bubbles |
| **Drawing (AI)** | Deep inpainting with LaMa AI + Real-ESRGAN upscaling | Complex backgrounds, drawings behind text |
| **Gradient** | Custom 2-color gradient fill | Bubbles with gradient backgrounds |
| **Pattern** | Tile-based fill from surrounding area | Textured backgrounds |
| **Manual** | Solid color fill | When you know the exact color needed |

**Gradient mode:** When selected, additional controls appear to set the start/end colors and direction (vertical, horizontal, diagonal).

#### Text styling (TextFormatBar)
The bar below the top bar lets you customize how your translated text looks:

| Control | Description |
|---------|------------|
| **Font** | Choose from 30+ built-in fonts or add your own .ttf files |
| **Size** | Font size (8 to 48) |
| **B / I** | Bold and Italic toggles |
| **Alignment** | Left, Center, or Right |
| **Color (A)** | Text color picker with 18 presets + custom color |
| **Gradient** | Text gradient with direction (vertical, horizontal, diagonal) + end color |
| **Shadow (S)** | Text shadow with blur intensity, X/Y offset, and color |

**Tip:** The style is remembered — new bubbles inherit the last style you used.

#### Bubble manipulation
When a bubble is selected (active), three handles appear on the image:

- **Purple circle (top)** — Drag to **rotate** the bubble
- **Purple circle ✛ (center)** — Drag to **move** the bubble
- **Yellow square ⤡ (bottom-right)** — Drag to **resize** the bubble

You can also adjust rotation with the **slider** in the bubble card.

#### Preview
Click the **eye icon** 👁 on any bubble card to see a real-time preview of your translated text on the image, with all styling applied (font, color, gradient, shadow).

The preview background color can be changed in **⚙ Info > Preview > Background color**.

### Step 4 — Export

1. Click **"Export"** in the top bar
2. Wait for the progress overlay to complete
3. A folder named `YourFolder_trad` is created **next to** your original folder
4. It contains all pages with translated text injected

**What happens during export:**
- Pages with translations: original text is removed (inpainted) and replaced with your styled translation
- Pages without translations: copied as-is to the output folder

### Settings (⚙ Info)

Click **"⚙ Info"** in the top bar to access:

| Setting | Description |
|---------|------------|
| **Interface language** | Switch between French, English, Spanish |
| **Manga name** | Name of the manga/manhwa |
| **Chapter number** | Chapter number |
| **Translator** | Your name/pseudo |
| **Source/Target language** | OCR and translation languages |
| **Default style** | Default text style for new bubbles |
| **Preview background** | Background color for the eye preview |
| **Custom fonts** | Load your own .ttf/.otf font files |

### Custom fonts

1. Go to **⚙ Info > Custom fonts**
2. Click **"+ Add a font (.ttf)"**
3. Select a `.ttf` or `.otf` file from your computer
4. The font appears in all font dropdowns with a ★ symbol
5. It works in both the preview (eye icon) and the final export
6. Custom fonts are saved in your project file and reloaded automatically

### Save & Auto-save

- Your work is **automatically saved** as a `.manhwatl.json` file in the chapter folder
- When you reopen the same folder, your translations, styles, and settings are restored
- The save indicator in the top bar shows: **●** (unsaved) or **✓ Saved**
- Press `Ctrl+S` to force save

---

## Features

### OCR & Text Detection
- Automatic text detection powered by **EasyOCR** (Korean, Japanese, Chinese, English)
- Manual zone selection with the **pencil tool** (rectangle, ellipse, diamond shapes)
- **Batch detection** for manually drawn zones
- Confirmation dialog before launching OCR (warns about processing time)

### 5 Inpainting Modes
- **Bubble** — Median background color fill
- **Drawing (AI)** — LaMa deep inpainting + Real-ESRGAN upscaling
- **Gradient** — Custom 2-color gradient fill with 4 directions
- **Pattern** — Tile-based fill from surrounding area
- **Manual** — Solid color fill

### Text Styling
- 30+ built-in fonts + custom .ttf loading
- Font size, bold, italic, alignment (left/center/right)
- Text color with gradient support (4 directions + start/end colors)
- Text shadow with blur, offset X/Y, and color controls
- Real-time preview with the eye icon 👁
- Default style presets & last-used style memory

### Bubble Manipulation
- 3 mask shapes: rectangle, ellipse, diamond
- Rotation handle + slider (snap to 5°)
- Drag to move ✛ and resize ⤡ handles
- Per-bubble inpainting mode and gradient background settings

### UI/UX
- Vertical scroll reader for natural manhwa reading
- Loading overlay with progress bar during OCR and export
- Confirmation dialogs before heavy operations
- Auto-save with JSON project files
- Internationalization (French, English, Spanish)
- Auto-detection of system language

---

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+O` | Open a chapter folder |
| `Ctrl+S` | Force save |
| `Ctrl+D` | Toggle pencil/draw mode |
| `Ctrl+B` | Toggle bold (if bubble selected) or toggle overlays |
| `Ctrl+I` | Toggle italic (if bubble selected) |

---

## FAQ

**Q: The app shows "OCR engine unavailable" at startup**
A: The OCR engine (sidecar) takes a few seconds to load on first launch. Wait for the spinner to complete. If it fails, check that the installation is complete and try reinstalling.

**Q: OCR takes too long**
A: OCR processing time depends on the number and size of pages. For a 20-page chapter, expect 2-5 minutes. Use the pencil tool for faster, targeted detection.

**Q: The exported text doesn't look like the preview**
A: Make sure you're using a font that's available on your system. Custom fonts loaded via .ttf files work in both preview and export.

**Q: Can I use this for commercial translation?**
A: FronteraForge is free for personal use only. See the Terms of Use below.

**Q: My custom font doesn't show in the export**
A: Make sure you added the font via ⚙ Info > Custom fonts (not just installed on Windows). The font data is embedded in the save file and used during export.

---

## Terms of Use

By installing and using FronteraForge, you agree to the following terms:

### License
FronteraForge is **free for personal, non-commercial use**. Redistribution, modification, decompilation, or reverse engineering is strictly prohibited without prior written consent from the author.

### Limitation of Liability
The software is provided **"as is"** without any warranty. The author shall not be held liable for any damages resulting from the use of the software, including but not limited to: data loss, inaccurate translations, compatibility issues, or any direct/indirect damages.

### Translated Content
**You are solely responsible** for the content you translate with FronteraForge. The author is not liable for the use of the software to translate, modify, or distribute copyrighted content without authorization from the rights holders.

### Personal Data
FronteraForge **does not collect, transmit, or store any personal data**. All work data (translations, settings, custom fonts) remains local on your machine.

### Changes
The author reserves the right to modify these terms at any time. Changes take effect upon publication of a new version.

### Applicable Law
These terms are governed by French law.

The complete Terms of Use are displayed when you first launch the application and must be accepted to use the software. You can review them again at any time in the app.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Desktop framework | Tauri 2 (Rust) |
| Frontend | React 18 + Zustand |
| OCR engine | EasyOCR (Python sidecar) |
| Inpainting | LaMa + Real-ESRGAN (SRVGGNetCompact) |
| Text rendering | Pillow (export) + CSS (preview) |
| Build | Vite + PyInstaller + NSIS |

---

## Support

If you find FronteraForge useful, consider supporting the project:

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/jeunetaoist)

---

**Made with ❤️ by [Jeune Taoist](https://ko-fi.com/jeunetaoist)**
