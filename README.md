# Touch Bar Companion 💻

> **Add Touch Bar functionality to any Mac** — Menu bar app with customizable shortcuts, app switching, and workflow automation.

![Version](https://img.shields.io/badge/version-0.1.0-blue)
![Platform](https://img.shields.io/badge/platform-macOS%2014.0+-lightgrey)
![License](https://img.shields.io/badge/license-MIT-green)

---

## What It Does

Touch Bar Companion brings **Touch Bar-style controls to any Mac** — even models without a physical Touch Bar (2016-2023 MacBook Pros).

Instead of hardware-dependent Touch Bar items, this app lives in your **menu bar** and provides:

- **Quick app switching** with custom hotkeys
- **Workflow shortcuts** for frequently-used actions
- **Customizable icons** and branding
- **Settings panel** for personalization

**Perfect for:** Developers, power users, and anyone who wants keyboard-first workflow control without Touch Bar hardware.

---

## Download

**Latest Release:** [v0.1.0](https://github.com/rawbethwebsites/touchbar-companion/releases/tag/v0.1.0)

- **File size:** 667 KB
- **Format:** `.app` (zipped)
- **Code signing:** Ad-hoc (development)

---

## Requirements

| Requirement | Details |
|-------------|---------|
| **OS** | macOS 14.0 (Sonoma) or later |
| **Hardware** | Any Intel or Apple Silicon Mac |
| **Permissions** | Accessibility (for app switching) |

**Note:** Despite the name, this app does **not** require a physical Touch Bar. It works on **any Mac** with macOS 14.0+.

---

## Installation

### 1. Download

```bash
# Direct download from GitHub Releases
curl -LO https://github.com/rawbethwebsites/touchbar-companion/releases/download/v0.1.0/TouchBarCompanion-v0.1.0.zip
```

### 2. Install

```bash
# Unzip
unzip TouchBarCompanion-v0.1.0.zip

# Move to Applications
mv "Touch Bar Companion.app" /Applications/
```

### 3. First Launch

macOS will block unsigned apps by default. Bypass this:

```bash
# Option A: Right-click method
# 1. Right-click (or Control-click) on the app
# 2. Select "Open" from the context menu
# 3. Click "Open" in the warning dialog

# Option B: Terminal method (advanced)
xattr -cr /Applications/Touch\ Bar\ Companion.app
```

### 4. Grant Permissions

The app needs **Accessibility permission** to switch apps and trigger shortcuts:

1. Open **System Settings** → **Privacy & Security** → **Accessibility**
2. Click the **+** button
3. Navigate to `/Applications/Touch Bar Companion.app`
4. Toggle it **ON**

---

## Usage

### Menu Bar

Once running, Touch Bar Companion appears in your menu bar:

- **Click the icon** to open settings
- **Access quick actions** from the dropdown menu
- **See active shortcuts** and status

### Keyboard Shortcuts

Default shortcuts (customizable in settings):

| Action | Shortcut |
|--------|----------|
| Toggle App | `Cmd + Option + T` |
| Quick Switch 1 | `Cmd + Option + 1` |
| Quick Switch 2 | `Cmd + Option + 2` |
| Open Settings | `Cmd + Option + ,` |

### Settings Panel

Customize your experience:

- **Icon size:** 20px - 44px
- **Touch Bar position:** Left, Center, Right (for future Touch Bar support)
- **Logo link:** Custom URL for branding
- **Hotkeys:** Enable/disable and remap shortcuts
- **Theme:** Light/Dark mode

---

## Building from Source

For developers who want to modify or rebuild:

### Prerequisites

- macOS 14.0+
- Xcode Command Line Tools (`xcode-select --install`)
- Swift 5.9+

### Build

```bash
git clone https://github.com/rawbethwebsites/touchbar-companion.git
cd touchbar-companion

# Run the build script
./build.sh
```

Output: `Touch Bar Companion.app` in the current directory.

### Project Structure

```
TouchBarCompanion/
├── main.swift              # Main app logic + SwiftUI settings
├── Predictions.swift       # Hotkey + app prediction logic
├── TextCompatibility.swift # Text rendering utilities
├── Assets/                 # Icons and images
├── build.sh                # Build script (no Xcode project needed)
└── README.md               # This file
```

---

## Troubleshooting

### App Won't Open

**Problem:** macOS says "App can't be opened because it's from an unidentified developer."

**Solution:**
```bash
xattr -cr /Applications/Touch\ Bar\ Companion.app
```

Or use the right-click → Open method described above.

### Touch Bar Items Don't Appear

**Problem:** No Touch Bar items show when app is running.

**Cause:** This app is designed for **menu bar use** on Macs **without** Touch Bar hardware. Touch Bar item support is planned for future versions.

**Workaround:** Use the menu bar icon and keyboard shortcuts instead.

### Shortcuts Don't Work

**Problem:** Keyboard shortcuts don't trigger actions.

**Solution:**
1. Check **System Settings** → **Keyboard** → **Keyboard Shortcuts** for conflicts
2. Ensure **Accessibility permission** is granted (see Installation step 4)
3. Restart the app after granting permissions

### App Crashes on Launch

**Solution:**
1. Check **Console.app** for crash logs (filter by `TouchBarCompanion`)
2. Ensure macOS 14.0+ is installed (`sw_vers`)
3. Try rebuilding from source if you've modified the code

---

## Roadmap

### v0.2.0 (Planned)
- [ ] TBN branding integration (logo, colors)
- [ ] Custom app shortcut presets (Hermes, Xcode, VS Code)
- [ ] Workflow builder (chain multiple actions)

### v1.0.0 (Future)
- [ ] Actual Touch Bar support for equipped Macs
- [ ] iCloud sync for settings across devices
- [ ] Plugin system for third-party extensions
- [ ] Code signing + notarization for seamless installs

---

## Credits

- **Inspired by:** [loretoparisi/touchbar-https](https://github.com/loretoparisi/touchbar-https)
- **Built with:** Swift, SwiftUI, AppKit
- **Brand:** The Boost Nation (TBN)

---

## License

MIT License — see [LICENSE](LICENSE) for details.

**Built by TBN — 2026**

---

## Support

- **Issues:** [GitHub Issues](https://github.com/rawbethwebsites/touchbar-companion/issues)
- **Discussions:** [GitHub Discussions](https://github.com/rawbethwebsites/touchbar-companion/discussions)
- **Email:** rob@theboostnation.com

**Found a bug?** Open an issue with:
- macOS version
- Steps to reproduce
- Console.app crash log (if applicable)

**Feature request?** Start a discussion with your use case.
