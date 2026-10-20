<div align="center">

# PanoRA

**Local-First Desktop Productivity Workstation**  
*Instant Screenshots • 60 FPS Recording • On-Device OCR • Local Clipboard • Peer-to-Peer Drop*

[![macOS](https://img.shields.io/badge/macOS-13%2B%20(Ventura)-000000?logo=apple&logoColor=white)](https://uplif.app/panora)
[![Windows](https://img.shields.io/badge/Windows-10%20%2F%2011-0078D6?logo=windows&logoColor=white)](https://uplif.app/panora)
[![Privacy: Zero Telemetry](https://img.shields.io/badge/Telemetry-Zero%20Cloud-success)](https://uplif.app/privacy)
[![Storage: Local JSON](https://img.shields.io/badge/Storage-100%25%20Local-blue)](https://uplif.app)

[Official Website](https://uplif.app/panora) • [Download Releases](https://github.com/YOUR_GITHUB_USERNAME/panora/releases) • [Documentation](https://uplif.app/docs) • [Privacy Policy](https://uplif.app/privacy)

</div>

---

## 🔒 The Local-First Philosophy

Most modern screenshot and clipboard utilities silently upload your private tokens, credentials, and screen captures to cloud servers. **PanoRA is engineered with strict on-device data sovereignty:**

1. **Zero Cloud Telemetry:** No third-party tracking scripts, no Google Analytics, no background crash dump uploads containing personal files.
2. **Transparent Local Storage:** All your cards, clips, annotations, and metadata are saved in a clean, human-readable local JSON file on your machine (`pano.json`).
3. **100% On-Device AI / OCR:** Text extraction uses Apple Vision on macOS and native Windows OCR. No text or image data ever leaves your computer.
4. **Peer-to-Peer LAN Drop:** Sharing files between devices happens directly over your local Wi-Fi / LAN via P2P. No middleman relay servers.

---

## ⚡ Key Capabilities

* **Instant Annotation Studio:** Precision arrows, vector callout loupes, numbered step counters (1, 2, 3…), and non-destructive redaction blur.
* **Hardware-Accelerated 60 FPS Recording:** Capture silky-smooth workflows with native ScreenCaptureKit on macOS and Windows Graphics Capture. Includes timeline trimming and frame-accurate mosaic censorship.
* **Sub-Pixel Scrolling Panorama:** Stitch ultra-long web pages, design canvases, and terminal logs up to 10,000+ pixels with live minimap feedback.
* **Smart Clipboard Station:** Auto-detects URLs, colors, codes, tasks, and media. Hit `Enter` to paste instantly into any active application.
* **System Color Loupe:** Pixel-accurate screen magnifier exporting directly to HEX, RGB, HSL, and Tailwind CSS tokens.

---

## 📥 Official Downloads & Binary Verification

Always verify binary authenticity using SHA-256 checksums before running:

| Platform | Architecture | Installer | Minimum OS |
| :--- | :--- | :--- | :--- |
| **macOS** | Apple Silicon (`arm64`) | [Download .dmg](https://uplif.app/panora) | macOS 13+ (Ventura, Sonoma, Sequoia) |
| **Windows** | 64-bit (`x64`) | [Download .exe](https://uplif.app/panora) | Windows 10 (1903+) / Windows 11 |

### Verify Checksum in Terminal

**macOS:**
```bash
shasum -a 256 PanoRA-0.1.0-universal.dmg

Windows (PowerShell):

Get-FileHash -Algorithm SHA256 "PanoRA Setup 0.1.0.exe"

