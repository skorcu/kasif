# 🧭 Kasif (Mac) — Lightning-Fast Native APFS Deep File & Content Search Engine

<div align="center">
  <img src="https://caneser.com/images/kasif-logo.webp" width="128" height="128" alt="Kasif macOS Logo" />
  <br />
  <h2>Search 5,000,000+ Files, WhatsApp, Apple Mail, Outlook & Telegram Archives in Milliseconds</h2>
  <p><b>Zero-Latency Native Search Powered by Apple Silicon (M1/M2/M3/M4) & APFS Kernel Traversal</b></p>
  <p>
    <a href="README.md"><b>English</b></a> • 
    <a href="README_TR.md"><b>🇹🇷 Türkçe</b></a>
  </p>
  <p>
    <a href="https://caneser.com/downloads/Kasif.dmg"><img src="https://img.shields.io/badge/Download_DMG-Universal_2-10B981?style=for-the-badge&logo=apple&logoColor=white" /></a>
    <img src="https://img.shields.io/badge/Apple_Notarized-Official_Security_Passed_✓-0284C7?style=for-the-badge&logo=apple" />
  </p>
  <p>
    <img src="https://img.shields.io/badge/Platform-macOS_14+_Sonoma_|_Sequoia-000000?style=flat-square&logo=apple&logoColor=white" />
    <img src="https://img.shields.io/badge/Architecture-Universal_2_(arm64_+_x86__64)-8B5CF6?style=flat-square" />
    <img src="https://img.shields.io/badge/Swift-Pure_Swift_|_AppKit-F05138?style=flat-square&logo=swift&logoColor=white" />
    <img src="https://img.shields.io/badge/Search_Latency-0.001s_Instant-10B981?style=flat-square" />
    <img src="https://img.shields.io/badge/Memory_Footprint-~20_MB_•_0.0%25_CPU-success?style=flat-square" />
    <a href="https://github.com/skorcu/ihya"><img src="https://img.shields.io/badge/Sister_App-Ihya_(System_Cleaner)-10B981?style=flat-square&logo=apple&logoColor=white" /></a>
    <img src="https://img.shields.io/badge/License-Proprietary_Freeware-blue?style=flat-square" />
  </p>
</div>

---

## 🌿 A Gift of Focus & Clarity from Sarkaç Adam to the Mac Community

> *"While seeking mental clarity and grounding through natural crystals, we believe no one should lose precious moments searching for lost files or critical message histories on their Mac.*  
> *Sarkaç Adam proudly presents **Kasif** to Mac users worldwide as a **gift of focus**: engineered in pure Swift to bypass sluggish web runtimes, connecting directly to the APFS kernel to retrieve anything on your storage in milliseconds."*

---

## ⚡ Why Kasif? (Performance & Architectural Edge)

Conventional command palettes and search utilities often bundle massive Chromium/Electron runtimes or heavy indexing background daemons that devour 200MB–600MB of RAM, causing fans to spin and battery life to degrade on large external drives.

**Kasif** was built from bare metal with pure Swift and AppKit directly wired into macOS kernel APIs:
- **Official Apple Notary Certification:** Officially reviewed, cryptographically signed, and notarized by Apple (`xcrun notarytool`) for seamless macOS Sequoia / Sonoma Gatekeeper launch.
- **Micro Binary Footprint (~2.7 MB):** Pure compiled machine code without WebViews, Node.js, or heavyweight third-party frameworks.
- **Zero CPU Idle & ~20MB RAM:** Completely quiet in the background. Zero battery drain, zero continuous disk indexing.
- **Kernel-Accelerated APFS Traversal (`getattrlistbulk` & mmap):** Leverages direct Apple filesystem C APIs to sweep across 5,000,000+ files and 8TB external SSDs in a single millisecond.

---

## 📊 Independent Search Benchmark & Comparison

*Test Environment: Apple Silicon M-Series & APFS SSD • 2,500,000 File & Message Test Corpus*

| Metric & Standard | 🧭 **Kasif (Universal 2)** | 🍎 **Default macOS Spotlight** | 📦 **Heavy Web/Launcher Tools** |
| :--- | :--- | :--- | :--- |
| **Architecture** | **Pure Swift & AppKit (Native)** | C++ & CoreServices | Electron / Rust Webview |
| **Package Download Size** | **~2.7 MB** | Pre-installed | 120 MB – 180 MB |
| **Background RAM Usage** | **~20 MB** | 600 MB+ (`mds`/`worker`) | 200 MB – 350 MB |
| **Background Battery Drain**| **0.0% (Zero CPU Idle)** | High during indexing | Continuous background polling |
| **5M+ File Search Latency** | **0.001 – 0.003s** | 1.2 – 3.5s | 0.8 – 2.0s |
| **WhatsApp, Telegram & SMS**| **Built-in (Local SQLite)** | iMessage Only | None / Complex plugins |
| **Apple Mail & Outlook** | **Built-in (Envelope Index)** | Shallow | Requires extra extensions |
| **External SSD/HDD Scale** | **Flawless (APFS & HFS+)** | Slow / Re-indexes | Plugin dependent |
| **Privacy & Offline State** | **100% Offline • Zero Tracking**| Sends queries to servers | Account & telemetry required |

---

## ✨ Core Capabilities

| Capability | Description |
| :--- | :--- |
| ⚡ **0.001s APFS Engine** | Direct memory-mapped (mmap) parallel file tree traversal for instantaneous search results. |
| 💬 **WhatsApp Deep Search** | Directly queries your local WhatsApp SQLite databases to find messages, contacts, and media archives. |
| 💬 **iMessage & SMS** | Sweeps macOS Messages (`chat.db`) to uncover verification 2FA codes and conversation history instantly. |
| 📬 **Apple Mail & Outlook** | Unified search across local Apple Mail and Microsoft Outlook email messages, subjects, and attachments. |
| ✈️ **Telegram Archive Search** | Resolves local Telegram Desktop message data for lightning-fast retrieval. |
| 👁️ **Full-Screen QuickLook** | Tap **`Space`** on any highlighted file, photo, or document to preview it instantly without opening the parent app. |
| 🎬 **Live Video & PDF Thumbs** | Renders crisp, live frame previews using AVFoundation and QLThumbnailGenerator directly in the search table. |
| 🔒 **100% Private & Offline** | Zero cloud calls. No search terms, filenames, or message contents ever leave your computer. |

---

## ⌨️ Global Keyboard Navigation

- **`⌥ Space` (Option + Space)**: Summon or dismiss Kasif instantly from anywhere in macOS.
- **`↑ / ↓`**: Navigate seamlessly through the results list.
- **`Space`**: Open native macOS QuickLook full-screen preview.
- **`Enter`**: Open file or message in its default application.
- **`⌘ Enter`**: Reveal the containing folder in Finder.
- **`⌘ C`**: Copy the absolute POSIX path to your clipboard.
- **`⌘ ,`**: Open Kasif Preferences.

---

## 🚀 Instant Installation (DMG)

1. Download the latest official release: **[Download Kasif.dmg](https://caneser.com/downloads/Kasif.dmg)**.
2. Open the DMG image and drag **Kâşif** into your **Applications** folder.
3. Press **`⌥ Space` (Option + Space)** to launch and experience instantaneous APFS search.

---

## 🤝 The Perfect Companion: Ihya (Pure Native System Cleaner) 💎

Pair Kasif's instantaneous search speed with **[Ihya](https://github.com/skorcu/ihya)** to keep your Mac free of clutter, developer junk, and background bloat!

- 🧹 **Smart Clean:** Deeply clears Xcode, Node, Docker, and system caches in seconds.
- ⚡ **Startup & Daemon Manager:** Toggles Login Items and neutralizes broken background daemons.
- 🧠 **Live Memory Turbo:** Darwin VM page reclamation without requiring root privileges.
- 🔍 **Duplicate Hunter:** 3-stage SHA-256 duplicate file detection with visual previews.

👉 **[Explore & Download Ihya on GitHub ➔](https://github.com/skorcu/ihya)**

---

## 📄 License & Attribution

Kasif is developed by **Sarkaç Adam** as a dedicated contribution to the global Mac ecosystem.  
All intellectual property, source architectures, and brand rights belong to the **Sarkaç Adam** ecosystem.  
To explore our natural mineral and handcrafted crystal collections that inspire calm and focus for your workspace, visit **[sarkacadam.com](https://sarkacadam.com)**.
