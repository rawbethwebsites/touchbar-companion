# Touch Bar Companion

**Built by The Boost Nation**

A familiar strip of controls, right on your screen.

Touch Bar Companion brings an on-screen, Touch Bar-style companion to Macs without a built-in Touch Bar. Keep typing suggestions, app shortcuts, volume controls, and editing actions together in a floating bar.

**A physical Touch Bar is not required. Hermes is one optional app shortcut; it is not required to use the companion.**

---

## ⚠️ Critical Requirements

**This build ONLY works on:**
- ✅ Apple Silicon Macs (M1, M2, M3 chips)
- ✅ macOS 26.0 or later

**Does NOT work on:**
- ❌ Intel Macs
- ❌ macOS 14, 15, or 25

This is a test build compiled for Apple Silicon only. Intel compatibility will be addressed in a future release.

---

## Download the test build

[**Download Touch Bar Companion v0.2.0**](https://github.com/rawbethwebsites/touchbar-companion/releases/download/v0.2.0/TouchBarCompanion-v0.2.0-no-xcode.zip) · 659 KB

**You do not need Xcode to run it.**

This repository distributes the compiled app, documentation, and images. App source code is not included.

---

## Install

1. **Download** and unzip the app
2. **Move** "Touch Bar Companion.app" into **Applications**
3. **Right-click → Open** (first time only — this is a development test build, so macOS may require approval in **System Settings → Privacy & Security → Open Anyway**)
4. **Enable Accessibility permission** for Touch Bar Companion in **System Settings → Privacy & Security → Accessibility** (required for suggestions and editing actions in other apps)
5. **Open the companion control panel** from the menu bar and use **Show / Hide Suggestions** to toggle the floating bar

**Keyboard shortcut:** `Control + Option + Command + T`

---

## Control Panel

Actual screenshot of the running app matching the v0.2.0 package:

![Touch Bar Companion control panel showing appearance, fading, position, and icon-size settings](https://raw.githubusercontent.com/rawbethwebsites/touchbar-companion/main/screenshots/control-panel.png)

The panel includes:
- Appearance controls (light/dark mode)
- Idle fading behavior
- Bar position (top/bottom of screen)
- Icon size adjustment
- App-shortcut selection

A verified image of the floating bar is still pending. Earlier HTML mockups are not screenshots of the app and are not presented as product images here.

---

## What to test

- Show and hide the floating bar
- Type in a compatible text field and check whether suggestions appear
- Try inserting a suggestion and using copy, paste, undo, and volume controls
- Open your selected apps from the bar
- Change appearance or position in the control panel and check the result

[**Report a problem**](https://github.com/rawbethwebsites/touchbar-companion/issues) with your Mac model, macOS version, the app you were typing in, and the steps that caused it. Avoid including private text in screenshots.

---

## Test-build limitations

- **Text suggestions and insertion** depend on the application and focused text field. Compatibility across apps is not fully verified
- This is a **custom on-screen companion** using Apple text services; it does not reproduce Apple's hardware Touch Bar interface exactly
- The package passes a **local code-signature verification**. Notarization and installation on a separate Mac have not been verified
- The release is labelled **v0.2.0**, but its internal app version is still **0.1.0**
- **macOS 26.0+ and arm64 requirements** were checked directly from the published executable on 2026-09-13

---

## Changelog

### v0.2.0 (2026-09-13)

**Removed:**
- Xcode dependency — no more installation warnings
- Touch Bar simulator toggle (developer-only feature)
- "Show / Hide Touch Bar" menu item

**Simplified:**
- Status bar now shows only Accessibility permission status
- Cleaner experience for non-developer users

### v0.1.0 (Initial test build)

- Initial release with TBN branding
- Menu bar app with floating suggestion bar
- Control panel for customization
- Keyboard shortcut support

---

Built by **The Boost Nation** — 2026

**TBN Brand Colors:** `#1a1210` (background), `#EA6113` (accent)
