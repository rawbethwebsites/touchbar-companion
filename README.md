# Touch Bar Companion

A native Swift/AppKit menu-bar application with a polished single-row custom TBN Touch Bar for developers. Apple text services power typing suggestions. No private APIs.

## Architecture

- **main.swift** — Menu-bar app, companion control panel (SwiftUI), global shortcut (⌃⌥⌘T), Quick Apps menu, system controls, and menu setup.
- **Predictions.swift** — Floating glass suggestion bar (NSVisualEffectView), Apple NSSpellChecker integration, typing playground, cross-app Accessibility polling, suggestion insertion, and all bar shortcut buttons.
- **TextCompatibility.swift** — Accessibility text-field discovery, secure-field filtering, UTF-16 range validation, text selection, and insertion helpers.
- **build.sh** — Builds, creates app icon set, and ad-hoc signs the app.

## Custom TBN Touch Bar

The floating bar is a single horizontal row with real vibrancy glassmorphism (NSVisualEffectView `.hud` material, subtle warm tint, hairline border). No up/down arrows, no popup menus, no row states — everything visible in one row.

**Left to right:**

| Section | Items |
|---|---|
| TBN logo | Clickable → opens theboostnation.com |
| Apple suggestions | 3 NSSpellChecker-powered prediction buttons |
| Developer shortcuts | Terminal, Hermes, ChatGPT, Comet |
| System actions | Screenshot to clipboard, Keyboard backlight settings |
| Volume | Volume down, Mute/unmute, Volume up |
| Edit controls | Emoji & symbols, Undo, Copy, Paste |

All icons are white SF Symbols on translucent rounded-rect tiles. Suggestion buttons show Apple's real prediction candidates when a compatible text field is focused.

## Verified shortcuts

- **Terminal** → `com.apple.Terminal` ✅
- **Hermes** → `com.nousresearch.hermes.setup` ✅ (corrected from `com.nousresearch.hermes`)
- **ChatGPT** → `com.openai.codex` ✅
- **Comet** → `ai.perplexity.comet` ✅
- **Xcode** → `com.apple.dt.Xcode` ✅
- **Screenshot** → `screencapture -i -c` (interactive to clipboard)
- **Volume ±/Mute** → AppleScript
- **Undo/Copy/Paste** → `sendAction` in playground, `CGEvent` with ⌘ modifier for external apps
- **Emoji** → `NSApp.orderFrontCharacterPalette`
- **Keyboard backlight** → opens System Settings → Keyboard

## Use

1. Open `Touch Bar Companion.app`.
2. Enable **Touch Bar Companion** in System Settings → Privacy & Security → Accessibility.
3. The floating bar appears at the bottom of the screen. Type in a compatible app to see Apple-powered suggestions.
4. Global shortcut: **⌃⌥⌘T** to show/hide suggestions. **⌃⌥1** to insert the first suggestion.

## Typing Playground

Menu → Typing Playground opens a standalone text editor. Type to see real NSSpellChecker candidates including inline predictions. Click a suggestion or press ⌃⌥1 to insert.

## Safety

- Secure/protected text fields are excluded.
- UTF-16 range validation on all text operations.
- Focused element and text are re-verified before any insertion.
- No text is stored, logged, or sent over the network.
- Apple's system text service handles all prediction requests.

## Build

```bash
cd TouchBarCompanion
./build.sh
```

Requires Xcode command-line tools. Output is a locally signed development build.

## Limitations

- Keyboard backlight control opens System Settings → Keyboard (direct backlight API is not public).
- Text-field compatibility varies by application.
- Xcode's Touch Bar simulator is separate and not embedded.
- The custom bar uses Apple text services for predictions, not Xcode's rendered Touch Bar UI.