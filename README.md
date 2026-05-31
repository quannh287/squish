# 🗜️ Squish
### A modern, 100% native SwiftUI clone of [Clop](https://github.com/FuzzyIdeas/Clop)

**Squish** is a lightning-fast, native media optimizer for Apple platforms (macOS / iOS). It silently monitors your clipboard or accepts drag-and-drop files, automatically compressing images and videos to save space and bandwidth without noticeable quality loss.

---

## 🌟 Acknowledgement & Inspiration

This project is a Swift/SwiftUI rewrite heavily inspired by **[Clop](https://github.com/FuzzyIdeas/Clop)** (created by [The low-tech guys](https://lowtechguys.com/)).

While Clop is a fantastic tool that relies on powerful external libraries like `FFmpeg` and `jpegoptim`, **Squish** was built from the ground up as an educational project with a different architectural philosophy: **100% Apple Native Frameworks**.

By replacing heavy CLI tools with Apple's native APIs, Squish aims to be incredibly lightweight and deeply integrated into the Apple ecosystem.

## 🚀 Key Features

*   **Clipboard Watcher:** Automatically detects and compresses large images/videos copied to your clipboard.
*   **Drag & Drop Zone:** A beautifully crafted SwiftUI floating window to quickly drop and squish files.
*   **Zero Third-Party Dependencies:**
    *   Uses **ImageIO** and **CoreGraphics** instead of `jpegoptim`/`pngquant`.
    *   Uses **AVFoundation** and Apple Silicon's Media Engine instead of `FFmpeg`.
*   **Modern Swift Architecture:** Built entirely with **SwiftUI** and modern **Swift Concurrency** (`async/await`, `Actors`) for buttery-smooth performance without blocking the main thread.

## 🛠️ Tech Stack

*   **Language:** Swift 5.9+
*   **UI Framework:** SwiftUI
*   **Media Processing:** `ImageIO`, `AVFoundation`, `CoreGraphics`
*   **Concurrency:** `Task`, `Actor`, Grand Central Dispatch (GCD)
*   **Architecture:** MVVM (Model-View-ViewModel)

## 📦 Getting Started

### Prerequisites
*   macOS 14.0+ (Sonoma) or iOS 17.0+
*   Xcode 15.0 or later

### Installation & Build
1.  Clone this repository:
```bash
git clone [https://github.com/yourusername/Squish.git](https://github.com/yourusername/Squish.git)
```
2.  Open `Squish.xcodeproj` in Xcode.
3.  Select your target (macOS or iOS).
4.  Hit `Cmd + R` to build and run.

## 🧠 Why rewrite it? (The Learning Journey)

This project serves as a practical deep dive into modern Apple development:
1.  **Transitioning UI:** Moving from AppKit (legacy macOS UI) to declarative **SwiftUI**.
2.  **Mastering Memory:** Learning to manage memory effectively when handling large media files in Swift.
3.  **Hardware Acceleration:** Understanding how to tap directly into Apple's Media Engine via AVFoundation for video encoding, vastly reducing battery drain and app size compared to software-based encoders.

## 📄 License

Following the footsteps of the original Clop project, Squish is open-sourced under the **GPL-3.0 License**. See the `LICENSE` file for more details.

*(Note: Any modifications or distributions of this project must also remain open-source under the same license).*
