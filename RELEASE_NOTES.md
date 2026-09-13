# Touch Bar Companion v0.2.0 — Test Build

**An on-screen Touch Bar-style companion for Macs without built-in Touch Bar hardware.**

**Built by The Boost Nation**

---

## Download

[**Download the app**](https://github.com/rawbethwebsites/touchbar-companion/releases/download/v0.2.0/TouchBarCompanion-v0.2.0-no-xcode.zip) (659 KB)

---

## ⚠️ Requirements

- **Apple Silicon Mac (arm64)** — M1, M2, or M3 chip required
- **macOS 26.0 or later** — Intel Macs and macOS 14/15/25 NOT supported
- **Accessibility permission** — Required for cross-app typing and editing features
- **No Xcode installation required** — Runs without developer tools

**Install:** Unzip, move the app to Applications, then open it. If macOS blocks the development build, review its approval option in **System Settings → Privacy & Security**. Enable the app under **Accessibility**.

Use **Show / Hide Suggestions** in the control panel or **Control + Option + Command + T** to toggle the floating bar.

---

## Control Panel

![Touch Bar Companion control panel](https://raw.githubusercontent.com/rawbethwebsites/touchbar-companion/main/screenshots/control-panel.png)

*Actual screenshot from v0.2.0 running on macOS 26.0+*

A verified floating-bar screenshot is still pending; HTML mockups are not actual app screenshots.

---

## What's New in v0.2.0

### Removed
- ❌ Xcode dependency — no more "Install Xcode" warnings
- ❌ Touch Bar simulator toggle (developer-only feature)
- ❌ "Show / Hide Touch Bar" menu item

### Simplified
- ✅ Status bar shows only Accessibility permission status
- ✅ Cleaner experience for non-developer users
- ✅ No confusing messages for non-developer users

---

## Verification and Limits — 2026-09-13

- ✅ The packaged executable matches the locally running app
- ✅ Local strict code-signature verification passed
- ✅ Control panel visually inspected
- ⚠️ Full cross-app interaction not verified
- ⚠️ Notarization not completed (Gatekeeper warning expected)
- ⚠️ Installation on another Mac not verified
- ⚠️ Internal app version remains 0.1.0 despite v0.2.0 release label

**Earlier claims of Intel and macOS 14 support were incorrect for this package.** This build is Apple Silicon only, macOS 26.0+.

---

## Archive Verification

**SHA-256:** `98e40582aa0a6f5b465cde0d3ef5026132b79a66f4d0af0f5cf05b9898ab51d5`

---

## Report Issues

Please report your **Mac model**, **macOS version**, **affected app**, and **reproduction steps** through [GitHub Issues](https://github.com/rawbethwebsites/touchbar-companion/issues).

---

**Built by The Boost Nation — 2026**

TBN Brand: `#1a1210` (background), `#EA6113` (accent)
