# PanoRA

Local-first desktop productivity workstation for macOS (Apple Silicon and Intel) and Windows 10/11.

PanoRA brings clipboard history, file referencing, screen capture, video recording, on-device OCR, PDF utilities, an encrypted local vault, and LAN peer-to-peer transfer into a single desktop workspace with zero cloud dependency.

- Website: [uplif.app/panora](https://uplif.app/panora)
- Pricing: [uplif.app/pricing](https://uplif.app/pricing)
- Privacy Policy: [uplif.app/privacy](https://uplif.app/privacy)
- Support: [support@uplif.app](mailto:support@uplif.app)

---

## Core Architecture

- **Zero-Duplication File Referencing:** Files and folders dropped into PanoRA are referenced by their original disk path rather than duplicated. External USB/SSD drives are detected and preserved when disconnected so cards remain intact when reconnected.
- **Local-First Persistence:** Cards, workspaces, and settings are stored locally (`pano.json`) using atomic writes with automatic `.bak` recovery.
- **No Telemetry:** No third-party analytics SDKs, no cloud accounts, and no outbound uploads of user content. Optional network calls are limited to license activation/verification and user-initiated update checks against `https://license.uplif.app`.
- **macOS and Windows Parity:** Built with native platform integrations on both operating systems (Apple Vision, AppKit, CoreGraphics, and SFSpeechRecognizer on macOS; WinRT OCR, Win32, and PowerShell helpers on Windows).

---

## Features

### Clipboard, Cards, and Organization
- **Automatic Clipboard Capture:** Collects text, links (with metadata preview), images, code snippets, files, folders, and color swatches into cards.
- **Sequential Paste Queue:** Queue multiple cards and paste them one by one into any target application (`Cmd+Option+V` / `Ctrl+Alt+V`) with a floating HUD controller.
- **Quick Look Overlay:** Instant spacebar preview for text, images, media, PDFs, files, and folders.
- **Workspaces and Tagging:** Custom workspaces, tag normalization with autocomplete, card color coding, sensitive content masking, and a Trash/Restore lifecycle.
- **11-Language Search Engine:** Operator-aware lexer/parser search across content, tags, types, and dates, plus a Command Palette (`Cmd+Shift+K` / `Ctrl+Shift+K`).

### Screen Capture, Image Editing, and Video Studio
- **Screenshots and Region Snip:** Native region capture with optional mockup frames and background presets.
- **Non-Destructive Annotator:** Canvas drawing tools, numbered step badges, arrows, shapes, magnification callouts, and permanent mosaic redaction while preserving the original raw image.
- **Scrolling Capture:** Capture full-length web pages, documents, and code views with automatic scroll stitching.
- **60 FPS Screen Recorder:** Hardware-accelerated screen and region recording (up to 4K/60 FPS on Pro/Team) with a standalone floating Recording HUD and resizable Webcam Bubble.
- **Video Studio:** Timeline trimming, crop, rotation, mosaic censor layers, keystroke shortcut overlay, and DSP audio cleanup (noise suppression and pitch control).
- **Watermark Studio:** Non-destructive photo and video watermarking.
- **Media Conversion:** Lossless/configurable WebP and AVIF image compression, plus M4A and MP3 audio extraction from video cards.
- **Pixel Loupe and Color Picker:** Screen magnifier copying colors in HEX, RGB, RGBA, HSL, Tailwind CSS, SwiftUI, Flutter, Android XML, and CSS variables.

### OCR, Voice, Text, and PDF Tools
- **On-Device OCR and QR/Barcode Reader:** Hardware-accelerated text recognition and QR/barcode scanning using Apple Vision (macOS) and WinRT OCR + pure JS decoding (Windows).
- **Voice Notes and Transcription:** Record voice cards with on-device speech-to-text and natural-language parsing.
- **Developer Text Tools and Export:** JSON formatting, line-break cleanup, Markdown stripping, and export to `.md`, `.txt`, `.csv`, and `.html`.
- **Smart Print Studio and Direct PDF Export:** Print-ready card layouts and single-click PDF export.
- **Zero-Dependency PDF Utilities:** Automatic PDF page count badges, plus pure-JS PDF page extraction (slicing) and multi-PDF merging.

### Encrypted Vault and Backups
- **AES-256-GCM Encrypted Vault:** Local vault encryption using `scrypt` key derivation, random IVs, and authentication tags. Decryption keys are cleared from memory immediately on lock.
- **Biometric and PIN Unlock:** Touch ID support on macOS and PIN unlock on macOS and Windows, with configurable idle/sleep/blur auto-lock.
- **Emergency Recovery Key:** 16-character recovery key (`PANO-XXXX-...`) for PIN resets without cloud recovery servers.
- **Encrypted Local Backups:** Password-protected AES-256 `.pano-backup` archive export, inspection, and merge/replace restore.

### Local Network Sync and Transfer
- **Pano Mesh (LAN P2P):** Direct encrypted Mac-to-Windows and peer-to-peer card and file transfer over local Wi-Fi, with PIN pairing, replay protection, and a 24-hour offline delivery queue.
- **AirBridge Mobile Portal:** Ephemeral, token-authenticated local web portal paired via QR code for two-way text and file transfer with phones and tablets (no mobile app required).
- **Pano Drop and AirDrop:** Temporary Wi-Fi QR sharing on macOS and Windows, plus native AirDrop and macOS Share Menu integration.

### Tasks, Focus, and Desktop Utilities
- **Tasks and Deadlines:** Due dates, completion tracking, Daily Digest summaries, and a floating Reminder HUD.
- **Pomodoro Focus Timer:** Built-in focus sessions with granular audio/haptic notification channels.
- **Desktop Helpers:** Ghost Drop Shelf (screen-edge drop zone), Floating Thumbnail Bar after capture, on-screen Sticky Notes, and Menu Bar / System Tray quick access.

---

## System Requirements

| Platform | Supported Versions | Architecture |
| :--- | :--- | :--- |
| **macOS** | macOS 13 (Ventura), 14 (Sonoma), 15 (Sequoia) and later | Universal Binary (Apple Silicon + Intel) |
| **Windows** | Windows 10 (1903+) and Windows 11 | x64 (NSIS installer, portable, zip) |

---

## Local Data Paths

All workspace data stays in standard OS application directories:

- **macOS:** `~/Library/Application Support/PanoRA/`
- **Windows:** `%APPDATA%\PanoRA\`

---

## Issues, Feedback, and Security

- Bug reports and feature requests: [github.com/uplifAPP/panora-desktop/issues](https://github.com/uplifAPP/panora-desktop/issues)
- Security vulnerabilities: see [SECURITY.md](https://github.com/uplifAPP/panora-desktop/blob/main/SECURITY.md) or email `security@uplif.app`
- General support: `support@uplif.app`
