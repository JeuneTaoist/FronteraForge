[![Download](https://img.shields.io/github/v/release/JeuneTaoist/FronteraForge?label=Download&color=7c5cfc&style=for-the-badge)](https://github.com/JeuneTaoist/FronteraForge/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/JeuneTaoist/FronteraForge/total?label=Downloads&color=7c5cfc&style=for-the-badge)](https://github.com/JeuneTaoist/FronteraForge/releases)


# FronteraForge

### [⬇️ Download the latest version](https://github.com/JeuneTaoist/FronteraForge/releases/latest)

**The all-in-one desktop translation studio for manhwa & manga.**

FronteraForge lets you translate manhwa/manga chapters with professional-quality text styling, AI-powered inpainting, and a seamless vertical reading workflow — all from a single desktop app. No internet required, everything runs locally on your machine.

> 🇫🇷 [Français](#-français) | 🇬🇧 [English](#-english) | 🇪🇸 [Español](#-español) — Interface auto-detected from your system language

---

# 🇬🇧 English

## Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Detailed Guide](#detailed-guide)
- [Features](#features)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [FAQ](#faq)
- [Terms of Use](#terms-of-use)
- [Tech Stack](#tech-stack)
- [Support](#support)

---

## Installation

### Windows (64-bit)

1. Download `FronteraForge_1.1.0_x64-setup.exe` from the [Releases](../../releases) page
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
| **None** | No modification | Testing, or background already clean |
| **Bubble (Solid)** | Fills with the median background color | White/solid color speech bubbles — recommended default |
| **Drawing (AI)** | Deep inpainting with LaMa AI + Real-ESRGAN upscaling | Simple backgrounds (flat colour, light gradient). **Avoid on complex artwork** — use the Cut tool instead |
| **Gradient** | Custom 2-color gradient fill | Bubbles with gradient backgrounds, thought/sound effect bubbles |
| **Pattern** | Tile-based fill from surrounding area | Shout bubbles, manga effects, textured backgrounds |
| **Manual** | Solid color fill | When you know the exact background color (HEX) |

**Advanced mode (per bubble):**
- **Background**: solid colour, gradient (4 directions), or imported image with interactive crop
- **Pattern**: 12 built-in tiles + custom PNG import, HQ recolouring (Rec.601), scale, opacity, gradient
- **Border**: colour or gradient, solid / dashed / dotted styles, 4× supersampling + LANCZOS

#### Text styling (TextFormatBar)

| Control | Description |
|---------|------------|
| **Font** | Choose from 30+ built-in fonts or add your own .ttf files |
| **Size** | Free font size from 1 to 1000 |
| **B / I** | Bold and Italic toggles |
| **Alignment** | Left, Center, or Right |
| **Color (A)** | Text color picker with 18 presets + custom color |
| **Gradient** | Text gradient with direction (vertical, horizontal, 2 diagonals) + end color |
| **Shadow (S)** | Text shadow with blur intensity, X/Y offset, and color |

**Tip:** The style is remembered — new bubbles inherit the last style you used.

#### Tail system (speech bubble pointer)

Each bubble can have a **tail** with 2 independent handles:

- **◉ Orange handle (tip)** — Drag anywhere on the image to pin the tip at an absolute position
- **■ Blue handle (base)** — Drag around the bubble to change the tail's exit point independently of the tip
- **Free mode** (no handles set): SVG dial + angle slider (0–359°) + length slider (up to 200%)
- Base always inset 15% into the shape for a seamless gap-free join
- **"Release"** button to return to free mode at any time

#### Bubble manipulation

When a bubble is selected (active), three handles appear on the image:

- **Purple circle (top)** — Drag to **rotate** the bubble (independent rotation per bubble)
- **Purple circle ✛ (center)** — Drag to **move** the bubble
- **Yellow square ⤡ (bottom-right)** — Drag to **resize** the bubble

You can also adjust rotation with the **slider** in the bubble card.

#### Cut / Replace tool

For complex backgrounds where inpainting isn't enough:

1. Select a region of the page
2. Export it and edit in an external editor (Photoshop, GIMP, **ChatGPT, DALL-E**, Adobe Firefly…)
3. Re-import the replacement — it is pasted at exact position on export
4. Multiple zones supported per page

> ⚠️ Never change the dimensions of the cut image.

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
- Text canvas auto-expands if text overflows the bubble (font size never auto-reduced)
- Custom fonts and patterns embedded as base64 in the save file

### Settings (⚙ Info)

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

- Your work is **automatically saved** as a `.manhwatl.json` file (v1.5) in the chapter folder
- When you reopen the same folder, your translations, styles, and settings are restored
- The save indicator in the top bar shows: **●** (unsaved) or **✓ Saved**
- Press `Ctrl+S` to force save
- Save files embed custom fonts and patterns as base64

---

## Features

### OCR & Text Detection
- Automatic text detection powered by **EasyOCR** (Korean, Japanese, Chinese, English)
- Manual zone selection with the **pencil tool** (rectangle, ellipse, diamond shapes)
- Batch detection for manually drawn zones
- Confirmation dialog before launching OCR

### 6 Inpainting Modes
- **None** — No modification
- **Bubble (Solid)** — Median background color fill
- **Drawing (AI)** — LaMa deep inpainting + Real-ESRGAN upscaling
- **Gradient** — Custom 2-color gradient fill with 4 directions
- **Pattern** — Tile-based fill from surrounding area
- **Manual** — Solid color fill

### Advanced Mode (per bubble)
- **Background**: solid colour, gradient (4 directions), or imported image with interactive crop
- **Pattern**: 12 built-in tiles + custom PNG import, HQ recolouring (Rec.601), scale, opacity
- **Border**: colour or gradient, solid / dashed / dotted styles, 4× supersampling + LANCZOS

### Text Styling
- 30+ built-in fonts + custom .ttf/.otf loading
- Free font size from 1 to 1000
- Bold, italic, alignment (left/center/right)
- Text color with gradient support (4 directions)
- Text shadow with blur, offset X/Y, and color
- Real-time preview with the eye icon 👁
- Default style presets & last-used style memory

### Tail System
- 2 independent handles: tip (◉ orange) and base (■ blue)
- Pin the tip anywhere on the image
- Base rotates independently around the bubble
- Free mode: SVG dial + angle slider + length slider
- Seamless join (base inset 15%)

### Cut / Replace Tool
- Select a region, export, edit externally, re-import at exact position
- Multiple zones per page
- Compatible with Photoshop, GIMP, ChatGPT, DALL-E, Adobe Firefly…

### Bubble Manipulation
- 3 mask shapes: rectangle, ellipse, diamond
- Independent rotation per bubble (handle + slider, snap to 5°)
- Drag to move ✛ and resize ⤡ handles
- Per-bubble inpainting mode and background settings

### UI/UX
- Vertical scroll reader for natural manhwa reading
- Loading overlay with progress bar during OCR and export
- Confirmation dialogs before heavy operations
- Auto-save with `.manhwatl.json` project files (v1.5)
- Home page with 4-step guide + Tutorial button (11-section modal)
- Dark theme
- Internationalization (French, English, Spanish) — auto-detection

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

**Q: When should I use AI inpainting vs the Cut tool?**
A: Use **Drawing (AI)** for simple backgrounds (flat colour, light gradients). For complex artwork or detailed illustrations behind text, use the **Cut / Replace** tool to edit the region in an external editor — the result will be much cleaner.

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

The complete Terms of Use are displayed when you first launch the application and must be accepted to use the software.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Desktop framework | Tauri v2 (Rust) |
| Frontend | React (JSX), Zustand, CSS-in-JS |
| Backend sidecar | Python 3.14, PyInstaller (onefile) |
| OCR engine | EasyOCR |
| Inpainting | LaMa (big-lama.pt) + Real-ESRGAN (SRVGGNetCompact) |
| Image processing | OpenCV, Pillow |
| Communication | stdin/stdout JSON (Rust ↔ Python) |
| Build | Vite + PyInstaller + NSIS |

---

## Support

If you find FronteraForge useful, consider supporting the project:

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/jeunetaoist)

---

---

# 🇫🇷 Français

## Table des matières

- [Installation](#installation-1)
- [Démarrage rapide](#démarrage-rapide)
- [Guide détaillé](#guide-détaillé)
- [Fonctionnalités](#fonctionnalités)
- [Raccourcis clavier](#raccourcis-clavier)
- [FAQ](#faq-1)
- [Conditions d'utilisation](#conditions-dutilisation)
- [Stack technique](#stack-technique)
- [Support](#support-1)

---

## Installation

### Windows (64-bit)

1. Téléchargez `FronteraForge_1.1.0_x64-setup.exe` depuis la page [Releases](../../releases)
2. Lancez l'installeur
3. **Lisez et acceptez les Conditions d'utilisation** (obligatoire pour utiliser l'app)
4. Lancez FronteraForge depuis votre bureau ou le menu Démarrer

### Configuration requise

- Windows 10 ou 11 (64-bit)
- ~500 Mo d'espace disque (inclut les modèles IA pour l'OCR et l'inpainting)
- Aucune connexion internet requise après installation

---

## Démarrage rapide

| Étape | Que faire |
|-------|----------|
| **1** | Cliquez sur **« Ouvrir »** et sélectionnez un dossier contenant vos images de chapitre (numérotées : 1.jpg, 2.jpg, ...) |
| **2** | Utilisez l'**outil crayon** ✏ pour dessiner des zones autour du texte, ou cliquez sur **« Lancer OCR »** pour la détection automatique |
| **3** | Tapez vos traductions dans le **panneau gauche**, choisissez votre style de texte et mode d'inpainting |
| **4** | Cliquez sur **« Exporter »** — un dossier `_trad` est créé à côté de votre dossier original avec toutes les pages traduites |

---

## Guide détaillé

### Étape 1 — Importer un chapitre

Cliquez sur le bouton **« Ouvrir »** (ou appuyez sur `Ctrl+O`) et sélectionnez un dossier contenant vos images manhwa/manga.

**Important :**
- Les images doivent être **numérotées** (1.jpg, 2.jpg, ... ou 001.png, 002.png, ...)
- Formats supportés : **JPG, PNG, WebP, BMP, TIFF**
- Les images sont affichées en **défilement vertical**, comme sur un téléphone
- L'app cherche automatiquement un fichier de sauvegarde (`.manhwatl.json`) dans le dossier

### Étape 2 — Détecter le texte

Vous avez **deux méthodes** :

#### Méthode A — OCR automatique (toutes les pages)
1. Cliquez sur **« Lancer OCR »** dans la barre du haut
2. Un dialogue de confirmation vous prévient que ça peut prendre du temps
3. Cliquez sur **« Lancer OCR »** pour confirmer
4. Attendez la fin de la barre de progression — l'app détecte automatiquement toutes les bulles
5. Les bulles détectées apparaissent en surimpression violette sur les images et en cartes dans le panneau gauche

#### Méthode B — Sélection manuelle (outil crayon)
1. Cliquez sur **« ✏ Crayon »** dans la barre du haut (ou `Ctrl+D`)
2. Choisissez une forme : **Rectangle**, **Ellipse**, ou **Losange**
3. Cliquez-glissez sur l'image pour dessiner une zone autour du texte
4. La zone est ajoutée comme bulle dans le panneau gauche
5. Cliquez sur **« Détecter (N) »** pour lancer l'OCR uniquement sur vos zones

**Astuce :** La méthode B est plus rapide et précise pour les manhwa avec des mises en page complexes. Utilisez la méthode A pour les manga standard avec des bulles bien délimitées.

### Étape 3 — Traduire et styliser

Chaque bulle détectée apparaît comme une **carte** dans le panneau gauche :

#### Traduction
- Le **texte original** (détecté par OCR) est affiché sur fond sombre
- Tapez votre **traduction** dans le champ texte en dessous
- Cliquez sur **« Confirmer »** quand vous êtes satisfait

#### Mode d'inpainting (suppression du texte original)

Choisissez dans le menu déroulant de chaque carte :

| Mode | Description | Idéal pour |
|------|------------|------------|
| **Aucun** | Aucune modification | Test, ou fond déjà propre |
| **Bulle (Solide)** | Remplissage avec la couleur médiane du fond | Bulles blanches / fond uni — recommandé par défaut |
| **Dessin (IA)** | Inpainting profond LaMa + upscaling Real-ESRGAN | Fonds simples (couleur unie, léger dégradé). **À éviter sur les dessins complexes** — utiliser l'outil Couper |
| **Dégradé** | Remplissage dégradé 2 couleurs | Bulles sur fond dégradé, bulles de pensée / effets sonores |
| **Pattern** | Remplissage par tuiles depuis la zone environnante | Bulles de cri, effets manga, fonds texturés |
| **Manuel** | Couleur unie | Quand vous connaissez la couleur exacte du fond (HEX) |

**Mode avancé (par bulle) :**
- **Fond** : couleur unie, dégradé (4 directions), ou image importée avec recadrage interactif
- **Pattern** : 12 motifs intégrés + import PNG custom, recoloration HQ (Rec.601), scale, opacité, dégradé
- **Bordure** : couleur ou dégradé, styles solid / dashed / dotted, supersampling 4× + LANCZOS

#### Style du texte (TextFormatBar)

| Contrôle | Description |
|----------|------------|
| **Police** | 30+ polices intégrées ou ajoutez vos propres .ttf |
| **Taille** | Taille libre de 1 à 1000 |
| **G / I** | Gras et Italique |
| **Alignement** | Gauche, Centre, ou Droite |
| **Couleur (A)** | Sélecteur de couleur avec 18 presets + couleur custom |
| **Dégradé** | Dégradé de texte (vertical, horizontal, 2 diagonales) + couleur de fin |
| **Ombre (S)** | Ombre portée avec intensité de flou, offset X/Y, et couleur |

**Astuce :** Le style est mémorisé — les nouvelles bulles héritent du dernier style utilisé.

#### Système de queue (pointe de bulle)

Chaque bulle peut avoir une **queue** avec 2 handles indépendants :

- **◉ Handle orange (pointe)** — Glissez n'importe où sur l'image pour fixer la pointe en position absolue
- **■ Handle bleu (base)** — Glissez autour de la bulle pour changer le point de sortie, indépendamment de la pointe
- **Mode libre** (sans handles fixés) : dial SVG + slider angle (0–359°) + slider longueur (jusqu'à 200%)
- La base est toujours incrustée à 15% dans la forme — fusion parfaite sans espace
- Bouton **« Libérer »** pour revenir en mode libre

#### Manipulation des bulles

Quand une bulle est sélectionnée, trois handles apparaissent sur l'image :

- **Cercle violet (haut)** — Glissez pour **tourner** la bulle (rotation indépendante par bulle)
- **Cercle violet ✛ (centre)** — Glissez pour **déplacer** la bulle
- **Carré jaune ⤡ (bas-droite)** — Glissez pour **redimensionner** la bulle

Vous pouvez aussi ajuster la rotation avec le **slider** dans la carte de la bulle.

#### Outil Couper / Remplacer

Pour les fonds complexes où l'inpainting ne suffit pas :

1. Sélectionnez une zone de la page
2. Exportez-la et éditez-la dans un logiciel externe (Photoshop, GIMP, **ChatGPT, DALL-E**, Adobe Firefly…)
3. Réimportez le remplacement — il est collé à la position exacte à l'export
4. Plusieurs zones supportées par page

> ⚠️ Ne jamais modifier les dimensions de l'image découpée.

#### Prévisualisation

Cliquez sur l'**icône œil** 👁 sur n'importe quelle carte pour voir un aperçu en temps réel de votre texte traduit sur l'image, avec tous les styles appliqués.

La couleur de fond de la prévisualisation peut être changée dans **⚙ Info > Aperçu > Couleur de fond**.

### Étape 4 — Exporter

1. Cliquez sur **« Exporter »** dans la barre du haut
2. Attendez la fin de l'overlay de progression
3. Un dossier `VotreDossier_trad` est créé **à côté** de votre dossier original
4. Il contient toutes les pages avec le texte traduit incrusté

**Ce qui se passe à l'export :**
- Pages avec traductions : le texte original est supprimé (inpainting) et remplacé par votre traduction stylisée
- Pages sans traductions : copiées telles quelles
- Le canvas texte s'étend automatiquement si le texte dépasse la bulle (taille jamais réduite)
- Polices et patterns custom embarqués en base64

### Paramètres (⚙ Info)

| Paramètre | Description |
|-----------|------------|
| **Langue de l'interface** | Basculer entre Français, English, Español |
| **Nom du manga** | Nom du manga/manhwa |
| **Numéro de chapitre** | Numéro du chapitre |
| **Traducteur** | Votre nom/pseudo |
| **Langue source/cible** | Langues OCR et traduction |
| **Style par défaut** | Style par défaut des nouvelles bulles |
| **Fond de prévisualisation** | Couleur de fond pour l'aperçu œil |
| **Polices custom** | Charger vos propres .ttf/.otf |

### Polices personnalisées

1. Allez dans **⚙ Info > Polices custom**
2. Cliquez sur **« + Ajouter une police (.ttf) »**
3. Sélectionnez un fichier `.ttf` ou `.otf`
4. La police apparaît dans tous les menus avec un symbole ★
5. Elle fonctionne en prévisualisation et à l'export
6. Les polices custom sont sauvegardées dans le fichier projet et rechargées automatiquement

### Sauvegarde & Auto-sauvegarde

- Votre travail est **automatiquement sauvegardé** en `.manhwatl.json` (v1.5) dans le dossier du chapitre
- À la réouverture du dossier, vos traductions, styles et paramètres sont restaurés
- L'indicateur dans la barre du haut affiche : **●** (non sauvé) ou **✓ Sauvé**
- Appuyez sur `Ctrl+S` pour forcer la sauvegarde
- Les fichiers de sauvegarde embarquent polices et patterns en base64

---

## Fonctionnalités

### OCR & Détection de texte
- Détection automatique via **EasyOCR** (coréen, japonais, chinois, anglais)
- Sélection manuelle avec l'**outil crayon** (rectangle, ellipse, losange)
- Détection par lot des zones manuelles
- Dialogue de confirmation avant le lancement de l'OCR

### 6 Modes d'inpainting
- **Aucun** — Aucune modification
- **Bulle (Solide)** — Remplissage couleur médiane
- **Dessin (IA)** — Inpainting profond LaMa + upscaling Real-ESRGAN
- **Dégradé** — Remplissage dégradé 2 couleurs, 4 directions
- **Pattern** — Remplissage par tuiles
- **Manuel** — Couleur unie

### Mode avancé (par bulle)
- **Fond** : couleur unie, dégradé (4 directions), ou image importée avec recadrage interactif
- **Pattern** : 12 motifs intégrés + import PNG custom, recoloration HQ (Rec.601), scale, opacité
- **Bordure** : couleur ou dégradé, solid / dashed / dotted, supersampling 4× + LANCZOS

### Style du texte
- 30+ polices intégrées + import .ttf/.otf
- Taille libre de 1 à 1000
- Gras, italique, alignement (gauche/centre/droite)
- Couleur + dégradé de texte (4 directions)
- Ombre portée (flou, offset X/Y, couleur)
- Prévisualisation temps réel avec l'icône 👁
- Presets de style & mémoire du dernier style

### Système de queue
- 2 handles indépendants : pointe (◉ orange) et base (■ bleu)
- Pointe fixable n'importe où sur l'image
- Base tourne indépendamment autour de la bulle
- Mode libre : dial SVG + slider angle + slider longueur
- Fusion parfaite (base incrustée à 15%)

### Outil Couper / Remplacer
- Sélectionner une zone, exporter, éditer en externe, réimporter à la position exacte
- Plusieurs zones par page
- Compatible Photoshop, GIMP, ChatGPT, DALL-E, Adobe Firefly…

### Manipulation des bulles
- 3 formes de masque : rectangle, ellipse, losange
- Rotation indépendante par bulle (handle + slider, snap 5°)
- Handles déplacer ✛ et redimensionner ⤡
- Mode d'inpainting et fond par bulle

### UI/UX
- Lecteur défilement vertical (lecture naturelle manhwa)
- Overlay de chargement avec barre de progression (OCR et export)
- Dialogues de confirmation avant les opérations lourdes
- Auto-sauvegarde `.manhwatl.json` (v1.5)
- Page d'accueil avec guide 4 étapes + bouton Tutoriel (modal 11 sections)
- Thème sombre
- Multilingue (Français, English, Español) — auto-détection

---

## Raccourcis clavier

| Raccourci | Action |
|-----------|--------|
| `Ctrl+O` | Ouvrir un dossier de chapitre |
| `Ctrl+S` | Forcer la sauvegarde |
| `Ctrl+D` | Basculer le mode crayon/dessin |
| `Ctrl+B` | Basculer gras (si bulle sélectionnée) ou basculer les overlays |
| `Ctrl+I` | Basculer italique (si bulle sélectionnée) |

---

## FAQ

**Q : L'app affiche « Moteur OCR indisponible » au démarrage**
R : Le moteur OCR (sidecar) prend quelques secondes à charger au premier lancement. Attendez la fin du spinner. En cas d'échec, vérifiez que l'installation est complète et réinstallez.

**Q : L'OCR prend trop de temps**
R : Le temps de traitement dépend du nombre et de la taille des pages. Pour un chapitre de 20 pages, comptez 2 à 5 minutes. Utilisez l'outil crayon pour une détection plus rapide et ciblée.

**Q : Le texte exporté ne ressemble pas à la prévisualisation**
R : Vérifiez que vous utilisez une police disponible sur votre système. Les polices custom chargées via .ttf fonctionnent en prévisualisation et à l'export.

**Q : Puis-je utiliser ceci pour de la traduction commerciale ?**
R : FronteraForge est gratuit pour un usage personnel uniquement. Voir les Conditions d'utilisation.

**Q : Ma police custom n'apparaît pas à l'export**
R : Vérifiez que vous l'avez ajoutée via ⚙ Info > Polices custom (pas juste installée sur Windows). Les données de la police sont embarquées dans le fichier de sauvegarde.

**Q : Quand utiliser l'inpainting IA vs l'outil Couper ?**
R : Utilisez **Dessin (IA)** pour les fonds simples (couleur unie, légers dégradés). Pour les illustrations complexes derrière le texte, utilisez l'outil **Couper / Remplacer** dans un éditeur externe — le résultat sera bien meilleur.

---

## Conditions d'utilisation

En installant et utilisant FronteraForge, vous acceptez les conditions suivantes :

### Licence
FronteraForge est **gratuit pour un usage personnel et non commercial**. La redistribution, modification, décompilation ou ingénierie inverse est strictement interdite sans consentement écrit préalable de l'auteur.

### Limitation de responsabilité
Le logiciel est fourni **« tel quel »** sans aucune garantie. L'auteur ne saurait être tenu responsable de tout dommage résultant de l'utilisation du logiciel, y compris mais sans s'y limiter : perte de données, traductions inexactes, problèmes de compatibilité, ou tout dommage direct/indirect.

### Contenu traduit
**Vous êtes seul responsable** du contenu que vous traduisez avec FronteraForge. L'auteur n'est pas responsable de l'utilisation du logiciel pour traduire, modifier ou distribuer du contenu protégé par le droit d'auteur sans autorisation des ayants droit.

### Données personnelles
FronteraForge **ne collecte, ne transmet et ne stocke aucune donnée personnelle**. Toutes les données de travail (traductions, paramètres, polices custom) restent locales sur votre machine.

### Modifications
L'auteur se réserve le droit de modifier ces conditions à tout moment. Les modifications prennent effet à la publication d'une nouvelle version.

### Droit applicable
Ces conditions sont régies par le droit français.

Les conditions complètes sont affichées au premier lancement de l'application et doivent être acceptées pour utiliser le logiciel.

---

## Stack technique

| Couche | Technologie |
|--------|-------------|
| Framework desktop | Tauri v2 (Rust) |
| Frontend | React (JSX), Zustand, CSS-in-JS |
| Backend sidecar | Python 3.14, PyInstaller (onefile) |
| Moteur OCR | EasyOCR |
| Inpainting | LaMa (big-lama.pt) + Real-ESRGAN (SRVGGNetCompact) |
| Traitement image | OpenCV, Pillow |
| Communication | stdin/stdout JSON (Rust ↔ Python) |
| Build | Vite + PyInstaller + NSIS |

---

## Support

Si FronteraForge vous est utile, pensez à soutenir le projet :

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Soutenir-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/jeunetaoist)

---

---

# 🇪🇸 Español

## Tabla de contenidos

- [Instalación](#instalación)
- [Inicio rápido](#inicio-rápido)
- [Guía detallada](#guía-detallada)
- [Funcionalidades](#funcionalidades)
- [Atajos de teclado](#atajos-de-teclado)
- [FAQ](#faq-2)
- [Condiciones de uso](#condiciones-de-uso)
- [Stack técnico](#stack-técnico)
- [Soporte](#soporte)

---

## Instalación

### Windows (64-bit)

1. Descarga `FronteraForge_1.1.0_x64-setup.exe` desde la página [Releases](../../releases)
2. Ejecuta el instalador
3. **Lee y acepta las Condiciones de uso** (obligatorio para usar la app)
4. Inicia FronteraForge desde el escritorio o el menú Inicio

### Requisitos

- Windows 10 u 11 (64-bit)
- ~500 MB de espacio en disco (incluye modelos IA para OCR e inpainting)
- No se requiere conexión a internet después de la instalación

---

## Inicio rápido

| Paso | Qué hacer |
|------|----------|
| **1** | Haz clic en **"Abrir"** y selecciona una carpeta con las imágenes del capítulo (numeradas: 1.jpg, 2.jpg, ...) |
| **2** | Usa la **herramienta lápiz** ✏ para dibujar zonas alrededor del texto, o haz clic en **"Lanzar OCR"** para la detección automática |
| **3** | Escribe tus traducciones en el **panel izquierdo**, elige el estilo de texto y modo de inpainting |
| **4** | Haz clic en **"Exportar"** — se crea una carpeta `_trad` junto a tu carpeta original con todas las páginas traducidas |

---

## Guía detallada

### Paso 1 — Importar un capítulo

Haz clic en el botón **"Abrir"** (o pulsa `Ctrl+O`) y selecciona una carpeta con tus imágenes manhwa/manga.

**Importante:**
- Las imágenes deben estar **numeradas** (1.jpg, 2.jpg, ... o 001.png, 002.png, ...)
- Formatos soportados: **JPG, PNG, WebP, BMP, TIFF**
- Las imágenes se muestran en **desplazamiento vertical**, como leer en un teléfono
- La app buscará automáticamente un archivo de guardado (`.manhwatl.json`) en la carpeta

### Paso 2 — Detectar texto

Tienes **dos métodos**:

#### Método A — OCR automático (todas las páginas)
1. Haz clic en **"Lanzar OCR"** en la barra superior
2. Un diálogo de confirmación te avisará de que puede tardar
3. Haz clic en **"Lanzar OCR"** para confirmar
4. Espera a que se complete la barra de progreso — la app detectará todos los bocadillos automáticamente
5. Los bocadillos detectados aparecen con superposiciones violetas y como tarjetas en el panel izquierdo

#### Método B — Selección manual (herramienta lápiz)
1. Haz clic en **"✏ Lápiz"** en la barra superior (o `Ctrl+D`)
2. Elige una forma: **Rectángulo**, **Elipse**, o **Rombo**
3. Haz clic y arrastra en la imagen para dibujar una zona alrededor del texto
4. La zona se añade como bocadillo en el panel izquierdo
5. Haz clic en **"Detectar (N)"** para lanzar el OCR solo en tus zonas

**Consejo:** El método B es más rápido y preciso para manhwa con diseños complejos. Usa el método A para manga estándar con bocadillos bien definidos.

### Paso 3 — Traducir y estilizar

Cada bocadillo detectado aparece como una **tarjeta** en el panel izquierdo:

#### Traducción
- El **texto original** (detectado por OCR) se muestra sobre fondo oscuro
- Escribe tu **traducción** en el campo de texto inferior
- Haz clic en **"Confirmar"** cuando estés satisfecho

#### Modo de inpainting (eliminación del texto original)

Elige en el menú desplegable de cada tarjeta:

| Modo | Descripción | Ideal para |
|------|------------|------------|
| **Ninguno** | Sin modificación | Pruebas, o fondo ya limpio |
| **Burbuja (Sólido)** | Relleno con el color mediano del fondo | Bocadillos blancos / fondo plano — recomendado por defecto |
| **Dibujo (IA)** | Inpainting profundo LaMa + upscaling Real-ESRGAN | Fondos simples (color plano, degradado suave). **Evitar en ilustraciones complejas** — usar la herramienta Cortar |
| **Degradado** | Relleno degradado de 2 colores | Bocadillos sobre fondo degradado, bocadillos de pensamiento / efectos de sonido |
| **Patrón** | Relleno por baldosas desde el área circundante | Bocadillos de grito, efectos manga, fondos con textura |
| **Manual** | Color sólido | Cuando conoces el color exacto del fondo (HEX) |

**Modo avanzado (por bocadillo):**
- **Fondo**: color sólido, degradado (4 direcciones), o imagen importada con recorte interactivo
- **Patrón**: 12 motivos integrados + importación PNG custom, recoloración HQ (Rec.601), escala, opacidad, degradado
- **Borde**: color o degradado, estilos solid / dashed / dotted, supersampling 4× + LANCZOS

#### Estilo de texto (TextFormatBar)

| Control | Descripción |
|---------|------------|
| **Fuente** | 30+ fuentes integradas o añade tus propias .ttf |
| **Tamaño** | Tamaño libre de 1 a 1000 |
| **N / C** | Negrita y Cursiva |
| **Alineación** | Izquierda, Centro, o Derecha |
| **Color (A)** | Selector de color con 18 presets + color personalizado |
| **Degradado** | Degradado de texto (vertical, horizontal, 2 diagonales) + color final |
| **Sombra (S)** | Sombra con intensidad de desenfoque, offset X/Y, y color |

**Consejo:** El estilo se memoriza — los nuevos bocadillos heredan el último estilo usado.

#### Sistema de cola (punta del bocadillo)

Cada bocadillo puede tener una **cola** con 2 handles independientes:

- **◉ Handle naranja (punta)** — Arrastra a cualquier lugar de la imagen para fijar la punta en posición absoluta
- **■ Handle azul (base)** — Arrastra alrededor del bocadillo para cambiar el punto de salida, independientemente de la punta
- **Modo libre** (sin handles fijos): dial SVG + slider de ángulo (0–359°) + slider de longitud (hasta 200%)
- La base siempre está incrustada un 15% en la forma — unión perfecta sin espacio
- Botón **"Liberar"** para volver al modo libre

#### Manipulación de bocadillos

Cuando un bocadillo está seleccionado, tres handles aparecen en la imagen:

- **Círculo violeta (arriba)** — Arrastra para **rotar** el bocadillo (rotación independiente por bocadillo)
- **Círculo violeta ✛ (centro)** — Arrastra para **mover** el bocadillo
- **Cuadrado amarillo ⤡ (abajo-derecha)** — Arrastra para **redimensionar** el bocadillo

También puedes ajustar la rotación con el **slider** en la tarjeta del bocadillo.

#### Herramienta Cortar / Reemplazar

Para fondos complejos donde el inpainting no es suficiente:

1. Selecciona una zona de la página
2. Expórtala y edítala en un editor externo (Photoshop, GIMP, **ChatGPT, DALL-E**, Adobe Firefly…)
3. Reimporta el reemplazo — se pega en la posición exacta al exportar
4. Múltiples zonas soportadas por página

> ⚠️ Nunca cambies las dimensiones de la imagen recortada.

#### Vista previa

Haz clic en el **icono del ojo** 👁 en cualquier tarjeta para ver una vista previa en tiempo real del texto traducido sobre la imagen, con todos los estilos aplicados.

El color de fondo de la vista previa se puede cambiar en **⚙ Info > Vista previa > Color de fondo**.

### Paso 4 — Exportar

1. Haz clic en **"Exportar"** en la barra superior
2. Espera a que se complete el overlay de progreso
3. Se crea una carpeta `TuCarpeta_trad` **junto a** tu carpeta original
4. Contiene todas las páginas con el texto traducido incrustado

**Qué pasa al exportar:**
- Páginas con traducciones: el texto original se elimina (inpainting) y se reemplaza con tu traducción estilizada
- Páginas sin traducciones: copiadas tal cual
- El canvas de texto se expande automáticamente si el texto desborda el bocadillo (tamaño nunca reducido)
- Fuentes y patrones custom incrustados como base64

### Ajustes (⚙ Info)

| Ajuste | Descripción |
|--------|------------|
| **Idioma de interfaz** | Cambiar entre Español, English, Français |
| **Nombre del manga** | Nombre del manga/manhwa |
| **Número de capítulo** | Número del capítulo |
| **Traductor** | Tu nombre/seudónimo |
| **Idioma origen/destino** | Idiomas OCR y traducción |
| **Estilo por defecto** | Estilo por defecto de los nuevos bocadillos |
| **Fondo de vista previa** | Color de fondo para la vista previa del ojo |
| **Fuentes custom** | Cargar tus propias .ttf/.otf |

### Fuentes personalizadas

1. Ve a **⚙ Info > Fuentes custom**
2. Haz clic en **"+ Añadir fuente (.ttf)"**
3. Selecciona un archivo `.ttf` o `.otf`
4. La fuente aparece en todos los menús con el símbolo ★
5. Funciona tanto en vista previa como en la exportación final
6. Las fuentes custom se guardan en el archivo del proyecto y se recargan automáticamente

### Guardado y autoguardado

- Tu trabajo se **guarda automáticamente** como `.manhwatl.json` (v1.5) en la carpeta del capítulo
- Al reabrir la carpeta, tus traducciones, estilos y ajustes se restauran
- El indicador en la barra superior muestra: **●** (sin guardar) o **✓ Guardado**
- Pulsa `Ctrl+S` para forzar el guardado
- Los archivos de guardado incorporan fuentes y patrones en base64

---

## Funcionalidades

### OCR y Detección de texto
- Detección automática mediante **EasyOCR** (coreano, japonés, chino, inglés)
- Selección manual con la **herramienta lápiz** (rectángulo, elipse, rombo)
- Detección por lotes de las zonas manuales
- Diálogo de confirmación antes del lanzamiento del OCR

### 6 Modos de inpainting
- **Ninguno** — Sin modificación
- **Burbuja (Sólido)** — Relleno color mediano
- **Dibujo (IA)** — Inpainting profundo LaMa + upscaling Real-ESRGAN
- **Degradado** — Relleno degradado 2 colores, 4 direcciones
- **Patrón** — Relleno por baldosas
- **Manual** — Color sólido

### Modo avanzado (por bocadillo)
- **Fondo**: color sólido, degradado (4 direcciones), o imagen importada con recorte interactivo
- **Patrón**: 12 motivos integrados + importación PNG custom, recoloración HQ (Rec.601), escala, opacidad
- **Borde**: color o degradado, solid / dashed / dotted, supersampling 4× + LANCZOS

### Estilo de texto
- 30+ fuentes integradas + importación .ttf/.otf
- Tamaño libre de 1 a 1000
- Negrita, cursiva, alineación (izquierda/centro/derecha)
- Color + degradado de texto (4 direcciones)
- Sombra (desenfoque, offset X/Y, color)
- Vista previa en tiempo real con el icono 👁
- Presets de estilo y memoria del último estilo

### Sistema de cola
- 2 handles independientes: punta (◉ naranja) y base (■ azul)
- Punta fijable en cualquier lugar de la imagen
- Base gira independientemente alrededor del bocadillo
- Modo libre: dial SVG + slider ángulo + slider longitud
- Unión perfecta (base incrustada 15%)

### Herramienta Cortar / Reemplazar
- Seleccionar una zona, exportar, editar en externo, reimportar en posición exacta
- Múltiples zonas por página
- Compatible con Photoshop, GIMP, ChatGPT, DALL-E, Adobe Firefly…

### Manipulación de bocadillos
- 3 formas de máscara: rectángulo, elipse, rombo
- Rotación independiente por bocadillo (handle + slider, snap 5°)
- Handles mover ✛ y redimensionar ⤡
- Modo de inpainting y fondo por bocadillo

### UI/UX
- Lector desplazamiento vertical (lectura natural manhwa)
- Overlay de carga con barra de progreso (OCR y exportación)
- Diálogos de confirmación antes de operaciones pesadas
- Autoguardado `.manhwatl.json` (v1.5)
- Página de inicio con guía de 4 pasos + botón Tutorial (modal de 11 secciones)
- Tema oscuro
- Multilingüe (Español, English, Français) — auto-detección

---

## Atajos de teclado

| Atajo | Acción |
|-------|--------|
| `Ctrl+O` | Abrir una carpeta de capítulo |
| `Ctrl+S` | Forzar guardado |
| `Ctrl+D` | Alternar modo lápiz/dibujo |
| `Ctrl+B` | Alternar negrita (si bocadillo seleccionado) o alternar overlays |
| `Ctrl+I` | Alternar cursiva (si bocadillo seleccionado) |

---

## FAQ

**P: La app muestra "Motor OCR no disponible" al iniciar**
R: El motor OCR (sidecar) tarda unos segundos en cargar en el primer inicio. Espera a que se complete el spinner. Si falla, verifica que la instalación esté completa y reinstala.

**P: El OCR tarda demasiado**
R: El tiempo de procesamiento depende del número y tamaño de las páginas. Para un capítulo de 20 páginas, espera de 2 a 5 minutos. Usa la herramienta lápiz para detección más rápida y dirigida.

**P: El texto exportado no se parece a la vista previa**
R: Asegúrate de que estás usando una fuente disponible en tu sistema. Las fuentes custom cargadas via .ttf funcionan tanto en vista previa como en exportación.

**P: ¿Puedo usar esto para traducción comercial?**
R: FronteraForge es gratuito solo para uso personal. Ver las Condiciones de uso.

**P: Mi fuente custom no aparece en la exportación**
R: Asegúrate de haberla añadido via ⚙ Info > Fuentes custom (no solo instalada en Windows). Los datos de la fuente se incrustan en el archivo de guardado.

**P: ¿Cuándo usar inpainting IA vs la herramienta Cortar?**
R: Usa **Dibujo (IA)** para fondos simples (color plano, degradados suaves). Para ilustraciones complejas detrás del texto, usa la herramienta **Cortar / Reemplazar** en un editor externo — el resultado será mucho más limpio.

---

## Condiciones de uso

Al instalar y usar FronteraForge, aceptas las siguientes condiciones:

### Licencia
FronteraForge es **gratuito para uso personal y no comercial**. La redistribución, modificación, descompilación o ingeniería inversa está estrictamente prohibida sin el consentimiento escrito previo del autor.

### Limitación de responsabilidad
El software se proporciona **"tal cual"** sin ninguna garantía. El autor no será responsable de ningún daño derivado del uso del software, incluyendo pero sin limitarse a: pérdida de datos, traducciones inexactas, problemas de compatibilidad, o cualquier daño directo/indirecto.

### Contenido traducido
**Eres el único responsable** del contenido que traduces con FronteraForge. El autor no es responsable del uso del software para traducir, modificar o distribuir contenido protegido por derechos de autor sin autorización de los titulares.

### Datos personales
FronteraForge **no recopila, transmite ni almacena ningún dato personal**. Todos los datos de trabajo (traducciones, ajustes, fuentes custom) permanecen locales en tu máquina.

### Modificaciones
El autor se reserva el derecho de modificar estas condiciones en cualquier momento. Los cambios entran en vigor con la publicación de una nueva versión.

### Ley aplicable
Estas condiciones se rigen por la ley francesa.

Las condiciones completas se muestran en el primer inicio de la aplicación y deben aceptarse para usar el software.

---

## Stack técnico

| Capa | Tecnología |
|------|------------|
| Framework desktop | Tauri v2 (Rust) |
| Frontend | React (JSX), Zustand, CSS-in-JS |
| Backend sidecar | Python 3.14, PyInstaller (onefile) |
| Motor OCR | EasyOCR |
| Inpainting | LaMa (big-lama.pt) + Real-ESRGAN (SRVGGNetCompact) |
| Procesamiento imagen | OpenCV, Pillow |
| Comunicación | stdin/stdout JSON (Rust ↔ Python) |
| Build | Vite + PyInstaller + NSIS |

---

## Soporte

Si FronteraForge te resulta útil, considera apoyar el proyecto:

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Apoyar-FF5E5B?logo=ko-fi&logoColor=white)](https://ko-fi.com/jeunetaoist)

---

---

**Made with ❤️ by [Jeune Taoist](https://ko-fi.com/jeunetaoist)**
