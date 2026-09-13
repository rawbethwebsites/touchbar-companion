# Touch Bar Companion — Release Notes

**Version:** 0.1.0  
**Release Date:** 2026-09-13  
**Build:** Initial public test release

---

## What's New

First public release of Touch Bar Companion — a menu bar app that brings Touch Bar-style workflow control to **any Mac**, regardless of Touch Bar hardware.

### Core Features

✅ **Menu Bar Integration**
- Lives in your menu bar for instant access
- Dropdown menu with quick actions
- Status indicators for active shortcuts

✅ **Keyboard Shortcuts**
- Customizable hotkeys for app switching
- Global shortcuts work from any app
- Conflict detection and remapping

✅ **Settings Panel**
- Icon size customization (20-44px)
- Touch Bar position settings (future-proof)
- Logo link configuration
- Hotkey enable/disable toggles
- Dark/Light theme support

✅ **TBN Branding**
- Custom TBN logo in app icon
- TBN color scheme in settings panel
- Branded download page

---

## What It's NOT

❌ **Not Touch Bar hardware dependent** — Works on any Mac with macOS 14.0+  
❌ **Not Hermes-specific** — General-purpose workflow tool (Hermes integration planned for v0.2.0)  
❌ **Not App Store ready** — Ad-hoc signed for testing only

---

## Known Issues

| Issue | Impact | Workaround | Planned Fix |
|-------|--------|------------|-------------|
| Ad-hoc code signing | Users must right-click → Open on first launch | Documented in README | v0.2.0: Notarization |
| No actual Touch Bar support | Touch Bar items don't appear on equipped Macs | Use menu bar + shortcuts | v1.0.0: Full Touch Bar API |
| Deprecation warnings (macOS 14 `onChange`) | Build warnings only, no runtime impact | None needed | v0.2.0: Code cleanup |

---

## Feedback Needed

Testing this release? Please report:

1. **Installation:** Did the app install and launch without issues?
2. **Shortcuts:** Do keyboard shortcuts work after granting Accessibility permission?
3. **UI:** Does the settings panel render correctly on your display resolution?
4. **Performance:** Any lag, crashes, or high CPU usage?
5. **Use Cases:** What workflows would you use this for?

**Submit feedback:**
- [GitHub Issues](https://github.com/rawbethwebsites/touchbar-companion/issues)
- Email: rob@theboostnation.com

---

## Next Release (v0.2.0)

Planned improvements:

- [ ] Code signing + notarization (no more right-click to open)
- [ ] TBN branding customization in settings UI
- [ ] Preset shortcut packs (Developer, Designer, Writer workflows)
- [ ] Workflow builder (chain multiple actions)
- [ ] Fix macOS 14 deprecation warnings

**Target date:** TBD based on v0.1.0 feedback

---

## Downloads

- **GitHub Release:** https://github.com/rawbethwebsites/touchbar-companion/releases/tag/v0.1.0
- **Vercel Demo Page:** https://vercel-deploy-sandy-gamma.vercel.app
- **Repository:** https://github.com/rawbethwebsites/touchbar-companion

---

**Built by TBN — 2026**
