# Kotoba User Manual

**Version**: 0.1.0
**Last Updated**: 2025-11-09
**Author**: Justin Chiu <meowhoo@gmail.com>

---

## 📋 Table of Contents

1. [About This Software](#1-about-this-software)
2. [System Requirements](#2-system-requirements)
3. [Installation](#3-installation)
4. [Initial Setup](#4-initial-setup)
5. [Features](#5-features)
   - 5.1 [Library Management](#51-library-management)
   - 5.2 [Screen Capture](#52-screen-capture)
   - 5.3 [OCR Recognition](#53-ocr-recognition)
   - 5.4 [Reading Mode](#54-reading-mode)
   - 5.5 [Translation Settings](#55-translation-settings)
   - 5.6 [Vocabulary Card System](#56-vocabulary-card-system)
6. [Keyboard Shortcuts](#6-keyboard-shortcuts)
7. [Frequently Asked Questions](#7-frequently-asked-questions)
8. [Troubleshooting](#8-troubleshooting)

---

## 1. About This Software

Kotoba is a tool designed specifically for **reading foreign novels**. It uses OCR to recognize novel content, paired with AI translation and a smart vocabulary card system, making it easy to read Japanese, English, and other foreign novels while learning the language.

### Main Features

- **🔍 Multilingual OCR Recognition**: Supports multilingual text recognition, auto-handles multi-column layouts, intelligently detects vertical/horizontal text
- **🤖 Multi-LLM Translation**: Integrates OpenAI, Claude, Gemini, Grok with customizable translation styles, character voices, and glossaries
- **📖 Smart Reading Modes**: Three reading modes (pure image, side-by-side, OCR text), with automatic vertical display for Chinese/Japanese
- **💬 AI Vocabulary Card System**: Auto-annotates pronunciation, translation, and examples via LLM, supports cross-book indexing and Anki export
- **🎨 Complete Theme & Language Support**: Light/Dark/System themes, Traditional Chinese/English bilingual interface

### Target Audience

- Readers who want to read foreign novels but need translation assistance
- Those who have novel files in image format (PNG, JPG, etc.)
- Language learners who want to build vocabulary cards while reading

---

## 2. System Requirements

### Minimum Requirements

- **Operating System**: Windows 10/11 (64-bit)
- **RAM**: Minimum 4GB
- **Disk Space**: Approximately 2GB
- **Network**: Internet connection required (for OCR and AI translation)

### Required Services

1. **Google Cloud Vision API** (for OCR text recognition)
   - Google Cloud account required
   - Project creation and Vision API activation required
   - JSON key file generation required

2. **AI Translation Service** (optional, for real-time translation)
   - OpenAI API (GPT-4, GPT-3.5)
   - Anthropic Claude API
   - Google Gemini API
   - xAI Grok API

---

## 3. Installation

Kotoba offers two installation methods. Choose based on your needs:

### Method 1: Installer Version (Recommended)

**Best for**: General users who want quick installation with Start Menu shortcuts

1. Go to the [Releases](https://github.com/meowhoo/kotoba/releases) page
2. Download the latest installer: `Kotoba-0.1.0-Setup.exe`
3. Double-click to run the installer
4. Choose installation location (default: `C:\Program Files\Kotoba`)
5. The application will launch automatically after installation
6. A `Kotoba` shortcut will be created in the Start Menu

> **Tips**:
> - On first launch, Windows Defender may show a warning. Click "Run anyway" or "More info" → "Run anyway"
> - Installation requires administrator privileges
> - You can customize desktop shortcuts and Start Menu location after installation

### Method 2: Portable Version

**Best for**: Advanced users who want to run from USB drives or avoid system installation

1. Go to the [Releases](https://github.com/meowhoo/kotoba/releases) page
2. Download the portable zip file: `Kotoba-0.1.0-win-x64.zip`
3. Extract to your desired location (e.g., `D:\Programs\Kotoba` or USB drive)
4. Navigate to the folder and find `Kotoba.exe`
5. Double-click to launch (no installation required)

> **Portable Version Benefits**:
> - No installation needed, extract and run
> - Can be run from USB drives anywhere
> - All settings and book data stored in application folder
> - Complete removal by simply deleting the folder

### Uninstallation

**Installer Version**:
Go to "Settings" → "Apps" → "Installed apps" → Find `Kotoba` → Click "Uninstall"

**Portable Version**:
Simply delete the extracted folder

---

## 4. Initial Setup

### Step 1: Configure Google Cloud Vision API

On first launch, you need to configure the Google Cloud Vision API key:

1. After entering the Library page, click the "System Settings" button (⚙️) in the top-right corner
2. In the "OCR Settings" section, find "Google Vision API Credentials"
3. Click the "📁" button to select the JSON key file you downloaded from Google Cloud
4. After configuration, click the "Save Settings" button

> **How to obtain a Google Cloud Vision API key?**
>
> 1. Go to [Google Cloud Console](https://console.cloud.google.com/)
> 2. Create a new project or select an existing project
> 3. **Enable billing account** (Required, credit card needed even for free tier)
> 4. Enable "Cloud Vision API"
> 5. Go to "IAM & Admin" → "Service Accounts"
> 6. Create a service account and download the JSON key file

### Step 2: Configure AI Translation Service (Optional)

If you need to use real-time translation features:

1. Find the "AI Settings" section in "System Settings"
2. Select your preferred AI service provider from the "Provider" dropdown (OpenAI / Anthropic / Google / xAI)
3. Enter the corresponding API key in the "API Key" field
4. Enter or select the model name in the "Model" field (e.g., gpt-4, claude-sonnet-4-20250514, gemini-2.0-flash-exp)
5. Click the "Save Settings" button

---

## 5. Features

### 5.1 Library Management

The library is your centralized management interface for all books.

#### Adding a Book

1. Click "Library" in the left navigation bar
2. Click the "+ Add Book" button in the top right corner
3. Fill in the book information:
   - **Book Name** (required)
   - **Author** (optional)
4. Click "OK" to complete the addition

> **Tip**: The book language will be automatically detected during the first OCR.

#### Setting Cover Image

1. Find the book you want to set a cover for in the library
2. Click the "⋯" quick menu in the top right corner of the book card
3. Select the "Cover" option
4. Upload an image file (supports JPG/PNG/WebP, max size 10MB)
5. The system will automatically adjust to 0.7:1 ratio and save

#### Editing Book Information

1. Find the book you want to edit in the library
2. Click the "⋯" quick menu in the top right corner of the book card, select "Edit"
3. You can modify the following:
   - **Book Name**: Title of the book
   - **Author**: Author's name
   - **Target Language**: Translation target language (Supported: Traditional Chinese, Simplified Chinese, English, Korean, Japanese, Spanish, German, French, Italian, Portuguese)
4. Click "Save" when finished

> **Tip**: After changing the target language, new translations will use the new language, but existing translations will not be automatically updated.

#### Deleting a Book

1. Click the "⋯" quick menu in the top right corner of the book card, select "Delete"
2. Confirm the deletion dialog
3. **Note**: Deleting a book will also delete all pages, OCR results, and related vocabulary card links

#### Start Reading

**Method 1: Double-click the Book Card**
- Double-click the book cover or card area to open the reading page

**Method 2: Use QuickMenu**
1. Click the "⋯" quick menu in the top right corner of the book card
2. Select the "Read" option

The system will remember your last reading progress. If this is your first time opening and there are no pages yet, you need to set up "Screen Capture" first.

---

### 5.2 Screen Capture

The screen capture feature allows you to quickly capture book page images.

#### Setting ROI (Region of Interest)

**What is ROI?**

ROI (Region of Interest) is the fixed area you want to capture. Once set, you can use global hotkeys for quick screenshots.

**Setup Steps:**

1. After opening a book, click "Capture" in the top toolbar
2. Press `Ctrl+F9` or click the "Set ROI" button
3. The screen will automatically minimize, showing a red semi-transparent selection box
4. Use your mouse to drag and select the area you want to capture
5. After releasing the mouse, the application will automatically return to the foreground and display a preview
6. Confirm that everything is correct, and the ROI setup is complete

#### Adding Pages

There are two ways to add book pages:

**Method 1: Using Global Hotkey for Screenshot**

1. Ensure ROI is set
2. Open your e-book software (e.g., Kindle, Adobe Reader)
3. Press the global hotkey `Ctrl+F10`
4. The system will automatically capture the ROI area and save it as a new page

**Method 2: Drag and Drop Images**

If you already have image files, you can directly drag and drop them:

1. Select an image file in File Explorer
2. Drag it to the large image area on the Capture page
3. Release the mouse, and the image will be automatically added as the last page
4. The system supports PNG, JPG, JPEG, WebP formats, max 10MB per file
5. Only one image can be uploaded at a time

> **Tip**: Newly uploaded images will be automatically numbered and added to the end. They cannot be inserted in the middle.

#### Image Management

**Drag to Reorder**

If the screenshot order is incorrect, you can drag to adjust:

1. In the left thumbnail list, click and hold the image you want to move
2. Drag it to the target position
3. Release the mouse, and the system will automatically renumber all image files

**Delete Images**

1. Click the "⋯" more options button in the top right corner of the thumbnail
2. Select "Delete"
3. After confirmation, the system will delete the image and automatically renumber

**Keyboard Navigation**

- Use `←` and `→` arrow keys to browse images
- The system will automatically scroll to the currently selected image

---

### 5.3 OCR Recognition

The OCR feature converts captured images into editable text.

#### Running OCR

1. Click the scope selection dropdown menu next to the "OCR" button in the top toolbar
2. Select the recognition scope:
   - **Current Page**: Only recognize the currently displayed page
   - **From Here to End**: Recognize from the current page to the last page
   - **All Pages**: Recognize all pages that have not been OCR'd
3. Click the "OCR" button to start recognition
4. The system will display a progress bar. You can press `Esc` or click "Cancel" at any time to interrupt
5. In dual-pane mode, the right side displays real-time text recognition results

#### Exclusion Zones

**Solving Traditional OCR's Biggest Pain Point**

Book pages often have page numbers, headers, footers, and book titles in the margins. These areas are a nightmare for traditional OCR tools—they get mixed into the main text, disrupt reading order, and even cause translation errors.

Kotoba's exclusion zone feature lets you precisely mark these unwanted areas. The system automatically skips them during OCR, completely solving this problem. The system provides two types:

**Global Exclusion Zones (Red)**

For fixed-position areas across all pages (e.g., page numbers or headers in the same location on every page)

1. Enable the "Show Exclusions" toggle button
2. Click the "➕ Add Global Exclusion" button in the bottom toolbar (or press `G`)
3. Drag on the preview image to select the area you want to exclude
4. After confirmation, the area will be marked with a red border and light red overlay
5. This exclusion zone will automatically apply to all pages

**Page-specific Exclusion Zones (Orange)**

For special areas on the current page only (e.g., illustrations or notes on a particular page)

1. Enable the "Show Exclusions" toggle button
2. Click the "➕ Add Page Exclusion" button in the bottom toolbar (or press `P`)
3. Drag on the preview image to select the area you want to exclude
4. After confirmation, the area will be marked with an orange border and light orange overlay
5. This exclusion zone only applies to the current page

**Advanced Features**

- **Copy/Paste Exclusion Zones**: Use `Ctrl+C` to copy the current page's exclusion zones, switch to another page, and use `Ctrl+V` to paste
- **Ignore Global Exclusions**: Check the "☑ Don't use global exclusions on this page" checkbox to disable global exclusion zones for the current page
- **Delete Exclusion Zones**: Select an exclusion zone and press `Delete` to remove it
- **Edit Exclusion Zones**: Click the border or corner of an exclusion zone to drag and adjust its size and position

After configuration, re-run OCR for changes to take effect.

#### Multi-language Support

Kotoba supports multilingual OCR recognition. The system will automatically select the corresponding OCR engine based on the book's language setting.

---

### 5.4 Reading Mode

Reading mode provides three display methods, which you can switch between using the top toolbar.

#### Image Mode (Pure Image)

1. Click the "Image" button
2. Displays the original book page image
3. Hover your mouse over words in the image to see vocabulary card tooltips
4. Click on a word to open the complete vocabulary card information

**Use Case**: View the original page layout while quickly accessing vocabulary cards you've created.

#### Image+TL Mode (Image + Translation)

1. Click the "Image+TL" button
2. The screen splits into two columns: left side shows the original image, right side shows AI translation
3. **Smart Layout**: The system automatically detects text direction, displaying Chinese/Japanese vertically and other languages horizontally
4. Drag the center divider to adjust the ratio between image and translation (20%-80%)
5. If the page already has OCR text, you can click the "Translate" button to call the LLM for translation
6. Translation results are cached and displayed directly on subsequent visits

**Use Case**: Compare the original image with translation to understand the full meaning of passages. Vertical display makes reading Chinese/Japanese more natural.

#### Text Mode (OCR Text + Word List)

1. Click the "Text" button
2. Left side displays OCR-recognized text
3. **Smart Layout**: The system automatically detects text direction, displaying Chinese/Japanese vertically and other languages horizontally
4. Right side shows a list of words appearing on this page
5. Select text and click the "+ Vocab Card" button to add vocabulary cards
6. Adjust font size (12-48px)

**Use Case**: Select and copy text, or add new vocabulary cards. Vertical display makes reading Chinese/Japanese more natural.

#### Page Navigation

- **Previous Page**: Click the left arrow or press the `Left Arrow Key`
- **Next Page**: Click the right arrow or press the `Right Arrow Key`
- **Go to Specific Page**: Click the page number input box, enter the page number, and press `Enter`

---

### 5.5 Translation Settings

Each book can have its own translation style, character voice settings, and glossary to make AI translations better suit your needs.

#### Opening Translation Settings

1. In the reading page, click the "Translation Settings" button in the top toolbar
2. A settings window with three tabs will open: Translation Style, Character Settings, Glossary

#### Translation Style Settings

**Temperature**
- Controls the creativity of the translation, range 0.0-1.0
- Lower values (e.g., 0.3): More precise and consistent translation
- Higher values (e.g., 0.8): More natural and varied translation
- Recommended value: 0.7

**Honorifics** (for Japanese source text)
- **Preserve**: Try to preserve the tone of honorifics
- **Convert**: Convert to modern Chinese polite expressions
- **Remove**: Convert to plain speech without honorifics

**Translation Constraints**
- Provide specific translation rules to the AI, one rule per line
- Click preset template buttons (S1-S5) to quickly apply common templates
- Templates include: Standard General, Colloquial Narrative, Literary Elegant, Light Novel, Technical Documentation, etc.
- You can freely edit the content after applying a template

Example constraints:
```
**Tone/Wording**: Neutral, clear, not exaggerated
**Rhythm/Sentence Length**: Medium sentence length; complex sentences no more than 2-3 clauses
**Dialogue/Inner Thoughts**: Natural dialogue but not overly colloquial
**Punctuation/Formatting**: Follow project punctuation standards; preserve original paragraphs and dialogue line breaks
```

#### Character Settings

Define speaking styles for main characters in the book. The AI will mimic these tones when translating dialogue.

1. Click the "+ Add Character" button
2. Enter the character name and tone description
3. Example:
   - **Protagonist**: "Young and straightforward, use less honorifics, casual tone"
   - **Teacher**: "Calm and dignified tone, use more honorifics"
4. You can edit or delete characters at any time

#### Glossary

Create fixed translations for proper nouns to ensure consistency throughout the book.

1. Click the "+ Add" button
2. Fill in:
   - **Source**: The term as it appears in the original text (e.g., 魔法)
   - **Target**: The desired translation (e.g., Magic)

---

### 5.6 Vocabulary Card System

The vocabulary card system is a word management feature independent of books.

#### Adding a Vocabulary Card

Vocabulary cards are automatically generated through AI annotation, including pronunciation, translation, and example sentences.

1. In **Text mode**, select the word or sentence you want to add
2. Click the "+ Vocab Card" button
3. The system will automatically call the LLM to generate the card content:
   - **Word/Phrase**: The text you selected
   - **Pronunciation**: Automatically annotated (e.g., Japanese kana)
   - **Translation**: AI automatic translation
   - **Example Sentence**: Context containing the word
4. The vocabulary card will be automatically saved and displayed on the page

#### Deleting a Vocabulary Card

1. Click the "Delete" icon on the right side of the vocabulary card
2. Confirm deletion

#### Search and Filter

- **Search**: Enter keywords in the search box at the top to search for words, translations, and example sentences
- **Filter by Book**: Click the filter dropdown menu, select a specific book, and display only vocabulary cards from that book

#### Export to Anki Deck

You can export vocabulary cards from a book to Anki `.apkg` format for review in Anki.

**Steps:**

1. In the library page, find the book whose vocabulary cards you want to export
2. Click the "⋯" quick menu in the top right corner of the book card
3. Select "Export Anki"
4. Click the "Export" button
5. The system will automatically generate a `.apkg` file and save it to your selected location
6. Open Anki, select "File" → "Import", and choose the generated `.apkg` file

---

## 6. Keyboard Shortcuts

### Global Hotkeys (Work even when the application is minimized)

| Hotkey | Function |
|--------|----------|
| `Ctrl+F9` | Set ROI (Region of Interest) |
| `Ctrl+F10` | Quick screenshot and add page |

### Reading Page Hotkeys

| Hotkey | Function |
|--------|----------|
| `←` | Previous page |
| `→` | Next page |

### General Hotkeys

| Hotkey | Function |
|--------|----------|
| `F11` | Full screen mode |

---

## 7. Frequently Asked Questions

### Q1: Windows shows a security warning on first run. What should I do?

This is normal because the software doesn't have a Microsoft code signing certificate. Follow these steps based on your system:

**Windows 10 / 11 - SmartScreen Warning**
1. When you see "Windows protected your PC" or "Microsoft Defender SmartScreen prevented an unrecognized app"
2. Click "More info"
3. Click "Run anyway"

**Windows 11 - Smart App Control (Stricter)**

If "Run anyway" is not available, Smart App Control is enabled:
1. Open Settings (Windows + I)
2. Go to Privacy & security → Windows Security → App & browser control
3. Click "Smart App Control settings"
4. Select "Off" (Note: Once turned off, you need to reset Windows to turn it back on)

**Alternative: Unblock the File**
1. Right-click on `Kotoba.exe` → Properties
2. At the bottom of the "General" tab, check "Unblock"
3. Click "Apply" → "OK"

### Q2: What if I can't successfully use Ctrl+F10 to capture screenshots?

**Solution: Use Drag and Drop Upload**

If you encounter issues with hotkey screenshots (e.g., hotkey conflicts, unable to set ROI, screenshot failures), you can use the drag and drop method instead:

1. **Manually capture or obtain images**
   - Use Windows built-in "Snipping Tool" (Win + Shift + S) to capture book pages
   - Or use other screenshot software (like Snagit, ShareX)
   - Or directly use existing book page image files

2. **Save as image file**
   - Save the screenshot as PNG, JPG, or WebP format
   - Ensure the file size does not exceed 10MB

3. **Drag and drop to Kotoba**
   - Open Kotoba's "Capture" page
   - Find the image file in File Explorer
   - Drag it directly to the large image area on the Capture page
   - Release the mouse, and the image will be automatically added to the book

4. **Repeat as needed**
   - Each image needs to be dragged and uploaded individually (one at a time)
   - The system will automatically number and add them to the end

**Advantages**:
- No need to set ROI
- Not dependent on global hotkeys
- Can use any screenshot tool
- Suitable for handling existing image files

### Q3: What if OCR recognition results are inaccurate?

**Possible Causes:**
- Image resolution is too low
- Image contains too much noise (background patterns, watermarks)

**Solutions:**
1. Ensure image resolution is at least 1024x768 or higher
2. Ensure the area selected during screenshot is complete and clear
3. Use the "Exclusion Zone" feature to exclude page numbers, illustrations, and other interference areas

### Q4: If I already have complete image files for a book and don't want to drag them one by one, what should I do?

**Answer: Place them directly in the book folder**

If you already have all the image files for a book, you can copy them directly to the book's `images/` directory:

**Steps:**

1. **Find the book folder**
   - Default location: `C:\Users\YourUsername\AppData\Roaming\kotoba\data\books\{bookId}`
   - Or check custom path in "System Settings" → "Folder Paths"

2. **Prepare image files**
   - Rename image files to: `page_0001.png`, `page_0002.png`, `page_0003.png`...
   - **Note**: File name format must be `page_` + 4 digits + `.png`
   - **Only PNG format is supported** (if JPG or other formats, convert to PNG first)

3. **Copy to images directory**
   - Copy all renamed image files to the `books\{bookId}\images\` directory

4. **Restart the application**
   - Close Kotoba
   - Reopen the application
   - Open the book, and you'll see all the images

**Example:**
```
books/my-book-123/images/
├── page_0001.png
├── page_0002.png
├── page_0003.png
├── page_0004.png
└── ...
```

> **Tip**: If you have many images, use batch renaming tools (like Windows PowerShell, Total Commander, etc.) to speed up the process.

### Q5: What if AI translation fails?

**Possible Causes:**
- API key is invalid or expired
- API quota exhausted
- Network connection issue

**Solutions:**
1. Go to "System Settings" to check if the API key is correct
2. Check if your API account still has a balance
3. Try switching to another AI service provider

### Q6: Why are hotkeys not working?

**Possible Causes:**
- Another application is using the same hotkeys
- The application did not register hotkeys correctly when in the background

**Solutions:**
1. Confirm that no other software is using `Ctrl+F9` or `Ctrl+F10`
2. Restart the application
3. Check if there are conflicting hotkey settings in Windows settings

### Q7: Can I recover a book after deleting it?

**Answer: No**

Deleting a book is a permanent operation that will also delete:
- All page images
- OCR recognition results
- Translation cache
- Book links for related vocabulary cards (the vocabulary cards themselves will be retained)

It is recommended to confirm that you really don't need the book's data before deleting it.

### Q8: Can I sync data across multiple computers?

**Yes, using cloud sync software**

Kotoba doesn't have built-in cloud sync functionality, but you can share your library across multiple computers using the following method:

**Setup Steps:**
1. Create a directory in your cloud sync folder (e.g., `D:\Dropbox\Kotoba\data` or `D:\Google Drive\Kotoba\data`)
2. In "System Settings" → "Folder Paths", point the book storage directory to that cloud sync folder
3. On other computers, repeat step 2, pointing to the same cloud folder path

This way, cloud sync software like Google Drive, Dropbox, or OneDrive will automatically sync your library, reading progress, and vocabulary cards, allowing you to use the same library across multiple computers.

---

## 8. Troubleshooting

### Application Won't Launch

1. Confirm that the operating system meets the requirements (Windows 10/11 64-bit)
2. Check if antivirus software is blocking it
3. Try "Run as Administrator"
4. Check `debug.log` (located at `C:\Users\YourUsername\AppData\Roaming\kotoba\debug.log`)

### OCR Keeps Failing

1. Confirm that the Google Cloud Vision API key is valid
2. Check if the Google Cloud project has enabled Vision API
3. Confirm that the account has remaining quota
4. Check if the network connection is normal

### Translation is Very Slow

1. Translation speed depends on the AI service provider's response speed
2. GPT-4 is usually slower than GPT-3.5, but the quality is better
3. Consider switching to Claude or Gemini
4. Translation results are cached and will be displayed immediately the second time you open the same page

### Application Still Has Residual Processes After Closing

1. Open "Task Manager" (`Ctrl+Shift+Esc`)
2. Find the `Kotoba.exe` or `python.exe` process
3. Click "End Task"
4. If the problem persists, please report it to the development team

---

## 💡 Usage Tips

### Efficient Screenshot Workflow

1. After setting up ROI, you can press `Ctrl+F10` continuously to quickly capture multiple pages
2. When taking screenshots, it is recommended to set the e-book software to "Single Page Display" mode

### Improve OCR Accuracy

1. Try to select the original image size when taking screenshots to avoid scaling
2. Use the "Exclusion Zone" feature to exclude page numbers and annotations
3. If OCR results have fixed error patterns, you can manually edit the TOML file


---

---

**Thank you for using Kotoba!**

Happy language learning! 📚✨
