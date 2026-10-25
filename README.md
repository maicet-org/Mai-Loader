# Mai-Loader

A modern desktop GUI for [yt-dlp](https://github.com/yt-dlp/yt-dlp) built with Kotlin and Jetpack Compose for Desktop. Mai-Loader simplifies downloading, processing, and tagging audio and video from supported media platforms while retaining granular control over quality, formats, and metadata.

---

## Features

### 🎬 Media Downloading & Conversion
- **Unified Interface:** Switch between Audio and Video modes with dedicated format selectors and quality presets.
- **Metadata Tagging:** Edit and embed Title, Author/Artist, Album, and Genre metadata directly into output files.
- **Embedded Assets:** Optional embedding of video thumbnails and subtitle tracks.
- **SponsorBlock Integration:** Automatically mark or remove sponsored segments during processing.
- **Fast URL Actions:**
  - One-click clipboard paste.
  - Quick download action (bypass metadata prefetch).
  - Press `Enter` to initiate downloads immediately.

### 📑 Playlist & Batch Processing
- **Interactive Carousel:** Horizontal thumbnail viewer with visual selection highlights and scroll indicators.
- **Item Counter:** Instant tally of loaded tracks/videos in a playlist.
- Individual item selection and batch queuing.

### 📥 Download Queue & Card Manager
- **Non-blocking Execution:** Concurrent background downloads powered by Kotlin Coroutines.
- **Real-time Metrics:** Displays download progress, transfer speed, percentage, and estimated time remaining (ETA).
- **Auto-dismiss Control:** Timed dismissal for completed (7s) and failed (15s) tasks, paused on mouse hover.
- **Quick Actions:** "Show in folder" for completed files and inline "Retry" for failed tasks.
- **Queue Overflow Badge:** Compact badge indicating queued items when exceeding 4 active cards.

### ⚙️ Dependency & App Management
- **Integrated Dependency Checker:** Monitors versions and status for `yt-dlp`, `ffmpeg`, and `deno`.
- **Dynamic Updates:** Update or install required binaries directly from the settings panel.
- **Application Updater:** Built-in check for new releases of Mai-Loader.
- **Session Persistence:** Option to persist the last entered URL across sessions.

---

## Tech Stack

- **Language:** Kotlin 2.4 (JVM Toolchain 21)
- **UI Framework:** Jetpack Compose Multiplatform (Desktop) & Material 3
- **Platform Integrations:** OpenJFX (Platform controls and file dialogs)
- **Concurrency & Serialization:** `kotlinx.coroutines`, `kotlinx.serialization`
- **Core Binaries:** `yt-dlp`, `ffmpeg`, `deno`

---

## Prerequisites

To run or build Mai-Loader, ensure the following are available or configured via the in-app **Settings** tab:

1. **yt-dlp**: Media extraction and download engine.
2. **FFmpeg**: Required for media merging, format conversion, and metadata embedding.
3. **Deno**: Required for advanced JavaScript extraction handling.

---

## Installation

### Windows Installer (Pre-built)
Download the latest `.msi` setup package from the [Releases](https://github.com/<TU-USUARIO>/<TU-REPO>/releases) tab and run the installer.

---

## Building from Source

### Requirements
- JDK 21 or higher.
- Gradle (wrapper included).

### Run in Development Mode
```bash
./gradlew run
```

### Build Windows Installer (.msi)
```bash
./gradlew packageMsi
```
The generated installer will be located in:
```
build/compose/binaries/main/msi/
```

---

## License

This project is open source. Refer to the `LICENSE` file for details.
