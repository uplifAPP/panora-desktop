# PanoRA

<div align="center">

**Local-First Desktop Productivity Workstation**  
*Instant Screenshots • 60 FPS Recording • On-Device OCR • Local Clipboard • Peer-to-Peer Transfer*

[![macOS](https://img.shields.io/badge/macOS-13%2B%20(Ventura%20%7C%20Sonoma%20%7C%20Sequoia)-000000?logo=apple&logoColor=white)](https://uplif.app/panora)
[![Windows](https://img.shields.io/badge/Windows-10%20(1903%2B)%20%2F%2011-0078D6?logo=windows&logoColor=white)](https://uplif.app/panora)
[![Privacy: Zero Telemetry](https://img.shields.io/badge/Telemetry-Zero%20Cloud-success)](https://uplif.app/privacy)
[![Storage: Local JSON](https://img.shields.io/badge/Storage-100%25%20Local%20JSON-blue)](https://uplif.app)
[![Architecture: Apple Silicon](https://img.shields.io/badge/Architecture-Universal%20%2F%20M1--M4-purple)](https://uplif.app/panora)

[Official Website](https://uplif.app/panora) • [Download Releases](https://github.com/uplif/panora/releases) • [Documentation](https://uplif.app/docs) • [Privacy Policy](https://uplif.app/privacy) • [Terms of Use](https://uplif.app/terms)

</div>

---

## 🔒 The Local-First Philosophy

Most modern screenshot and clipboard utilities silently upload your tokens, sensitive credentials, customer data, and screen captures to cloud servers. **PanoRA is engineered with strict, uncompromising on-device data sovereignty:**

1. **Zero Cloud Telemetry:** No third-party trackers, no behavioral analytics SDKs (no Google Analytics, no Mixpanel), and no automated telemetry uploads containing personal files.
2. **Transparent Local Storage:** All your cards, clips, annotations, and metadata are saved in a clean, human-readable local JSON file on your machine (`pano.json`). You can inspect, version-control, or back it up anytime.
3. **100% On-Device AI / OCR:** Text recognition runs entirely on your local GPU/CPU using native operating system frameworks (Apple Vision on macOS and native offline OCR on Windows). No optical or textual data is ever transmitted across the internet.
4. **Peer-to-Peer LAN Drop:** Sharing files between devices happens directly over your local Wi-Fi / LAN via P2P. No middleman relay servers inspect or retain your files.
5. **Full Offline Operation:** Unplug your Ethernet cable or disable Wi-Fi — PanoRA functions seamlessly with 100% capability.

---

## ⚡ Key Capabilities

### 🎥 Hardware-Accelerated 60 FPS Video Studio
* **Native Capture Engine:** Powered by Apple ScreenCaptureKit on macOS and Windows Graphics Capture for stutter-free 60 FPS recording with minimal CPU overhead.
* **Timeline Redaction Blur:** Apply frame-accurate timeline mosaic blur over private API tokens, customer credentials, or passwords before exporting.
* **Instant Trimming & Export:** Multi-format export to MP4, WebM, and lightweight animated GIF.

### 📸 Non-Destructive Annotation Studio
* **Sequential Step Badges:** Drop auto-incrementing numbered badges (1, 2, 3…) with a single click.
* **Callout Loupes & Arrows:** Pixel-aligned bezier guidance arrows and magnification callouts.
* **Mosaic Redaction Brush:** Permanently redact confidential regions directly on the canvas without altering your original screen resolution.

### 📜 Sub-Pixel Scrolling Panorama
* Stitch ultra-long web pages, code listings, and terminal logs up to 10,000+ pixels with live real-time visual overlap computation and minimap preview.

### 📋 Smart Clipboard & Task Station
* Collect text clips, code snippets, image assets, color swatches, and voice notes into organizeable cards.
* Smart parsing for tags (`#work`, `#todo`), deadlines (`@tomorrow 15:00`), and markdown formatting.
* Direct paste: hit `Enter` on any card to inject its contents directly into your active editor or messaging app.

### 🔍 Precision Color Loupe
* Real-time pixel magnifier with single-click clipboard copying in HEX, RGB, HSL, and Tailwind CSS format.

### 🎙️ On-Device Voice Transcriber
* High-speed speech-to-text powered by native system speech engines (Apple SFSpeechRecognizer & Windows Speech) with zero cloud dependencies.

---

## 📥 Official Downloads & Binary Verification

Always verify binary authenticity using SHA-256 checksums before running:

| Platform | Target Architecture | Package | Minimum OS Requirement | SHA-256 Checksum |
| :--- | :--- | :--- | :--- | :--- |
| **macOS** | Universal (Apple Silicon & Intel) | `PanoRA-0.1.0-universal.dmg` | macOS 13+ (Ventura, Sonoma, Sequoia) | `0f756d1c3c5ba2e112600a7f4303a63facd183994f45ad00219cf63803db4249` |
| **Windows** | x86_64 / 64-bit | `PanoRA Setup 0.1.0.exe` | Windows 10 (Build 1903+) / Windows 11 | `b1a08259157c70af858c016a9cc273cbf3b67a3d927cd54d373ce4342dd4608f` |

### How to Verify Checksums

**macOS (Terminal):**
```bash
shasum -a 256 PanoRA-0.1.0-universal.dmg
```

**Windows (PowerShell):**
```powershell
Get-FileHash -Algorithm SHA256 "PanoRA Setup 0.1.0.exe"
```

---

## ⌨️ Essential Keyboard Shortcuts

| Action | macOS | Windows |
| :--- | :--- | :--- |
| **Toggle PanoRA HUD** | `⌘ ⇧ Space` | `Ctrl + Shift + Space` |
| **Quick Search & Commands** | `⌘ ⇧ K` / `⌘ F` | `Ctrl + Shift + K` / `Ctrl + F` |
| **Screen OCR (Text Grab)** | `⌘ ⇧ O` | `Ctrl + Shift + O` |
| **Color Eyedropper Loupe** | `⌘ ⇧ C` | `Ctrl + Shift + C` |
| **Quick Voice Recording** | `⌘ ⇧ R` | `Ctrl + Shift + R` |
| **Paste from Clipboard to Card**| `⌘ ⇧ V` | `Ctrl + Shift + V` |
| **Quick Task Creation** | `⌘ ⇧ N` | `Ctrl + Shift + N` |
| **Switch Workspaces** | `⌘ 1`, `⌘ 2`, `⌘ 3`... | `Ctrl + 1`, `Ctrl + 2`, `Ctrl + 3`... |
| **Settings & Preferences** | `⌘ ,` | `Ctrl + ,` |

---

## 🛡️ Independent Privacy & Network Audit

We actively encourage security audits:
1. Launch **Wireshark**, **Little Snitch**, or **LuLu** on your workstation.
2. Filter network traffic by process name `PanoRA`.
3. Capture screens, run OCR text extractions, record video, and manage your clipboard.
4. You will observe **0 outbound packets** transmitting media, OCR text, or clipboard data.
5. Inbound traffic is strictly limited to optional user-initiated update checks against `https://license.uplif.app/updates`.

---

## 📁 Local Data Location

All your workspace data is stored in standard OS application folders:

* **macOS:** `~/Library/Application Support/PanoRA/pano.json`
* **Windows:** `%APPDATA%\PanoRA\pano.json`

You maintain complete ownership of your database. You can copy, back up, or delete it at any time with standard OS file managers.

---

## 💬 Community, Feedback & Support

* **Bug Reports:** Found an issue? [Open a Bug Report](https://github.com/uplif/panora/issues/new) with reproduction steps.
* **Feature Requests:** Have a suggestion? Share it on [GitHub Issues](https://github.com/uplif/panora/issues).
* **Website:** [uplif.app/panora](https://uplif.app/panora)
* **Direct Support:** `support@uplif.app`

---

<div align="center">
  <sub>Copyright © 2026 Uplif Studio. Built with privacy, speed, and elegance for creators and engineers.</sub>
</div>
