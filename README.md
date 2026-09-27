# Infinite Yield FE
<div align="center">
  <img src="https://github.com/DarkNetworks/Infinite-Yield/assets/108237499/285ff938-7de6-4ad4-811e-e451d2d92694" width="500" height="500" alt="Infinite Yield Logo">
</div>
Infinite Yield FE is a powerful FE admin script for Roblox that brings a host of exciting features for developers and players.

## Loadstring

Loadstring to execute Infinite Yield!
```lua
loadstring(game:HttpGet('https://raw.githubusercontent.com/DarkNetworks/Infinite-Yield/main/latest.lua'))()
```

## Features

- 🌐 **Support Server**: `discord / support / help` - Join the Infinite Yield support server and get assistance from the community.
- 💻 **Console**: `console` - Access the old Roblox console for advanced control.
- 🚀 **DEX by Moon**: `explorer / dex` - Open DEX by Moon and explore Roblox's inner workings.
- ⚙️ **Server Info**: `serverinfo / info` - Get insightful information about the server you are in.
- 🌐 **Server Hop**: `serverhop / shop` - Instantly teleport to a different server for new adventures.
- 🎮 **Join Player**: `joinplayer [username / ID] [place ID]` - Join a specific player's server and team up for fun.
- 👤 **Creator ID**: `creatorid / creator` - Discover the creator's ID behind the game you love.

**And much much more!**

- ⚙️ **VR Support**: `vr` - Use VR in all of the games you can think of!

## Interface & Accessibility (v5.9.4)

The main window, command bar, notifications, tooltips, settings panels, keybind
editor, plugin editor, part picker and logs window were audited for UI, UX and
accessibility and reworked without changing any command behavior.

### Keyboard shortcuts

| Keys | Action |
| --- | --- |
| `;` (prefix) | Focus the command bar |
| `Up` / `Down` | Move through matching commands (empty bar: command history) |
| `Tab` | Autocomplete the highlighted command |
| `Enter` | Run the typed command |
| `Esc` | Clear/blur the command bar, dismiss tooltip & notification, close floating editors |

### Command bar & command list

- Taller 26px rows with hover wash, truncation instead of clipped text, and a
  visible selection ring on the current match.
- A persistent status bar shows match counts (`12 matches`), empty states
  (`No matches for "xyz"`), total command count and keyboard hints.
- Descriptive placeholder (`Search commands (;)`) with a high-contrast hint
  color, plus a clear (x) button.
- Tab completes the *highlighted* row, not just the first text match.
- Commands disabled with `removecmd` are marked `(disabled)` in tooltips and
  removed from keyboard/gamepad focus.

### Notifications

- Queued (up to 4) so rapid messages are never overwritten or lost.
- Auto-dismiss pauses while hovered; pin keeps a message on screen.
- Progress bar shows remaining time; `Esc` or the 28px close button dismisses.
- No more leaked click connections (previously one per notification).

### Tooltips

- Opaque, higher-contrast, rounded, clamped inside the viewport, and no longer
  blocking clicks (`Active = false`).
- Every icon-only button (settings, reference, close, pin, collapse, clear…)
  now has a hover tooltip and an accessible name.
- Keyboard/gamepad selection mirrors the tooltip, so descriptions are never
  mouse-only.

### Settings & preferences

New persisted preferences in `IY_FE.iy` (Settings panel, bottom):

- **UI Scale** — cycles 85% / 100% / 115% / 130% via `UIScale` on every panel.
- **Reduce Motion** — disables tweens and skips the intro animation.
- **High Contrast** — black/white/yellow preset; your own theme is preserved
  underneath and restored when toggled off (edits made while it is on still
  save to your theme).

Related fixes: ON/OFF toggles now show **text labels** (never color alone),
all panel buttons meet the 24px minimum target size, previously invisible
scrollbars (thickness `0`) are visible and touch-friendly (10–12px), the
plugin file field uses a real placeholder with empty-submit validation, and
the intro splash is click/tap-to-skip.

### Accessibility statement

Targets WCAG 2.2 AA where the Roblox client allows: visible focus on every
control, 24px minimum touch targets, text-plus-color state (no color-only
meaning), `Tab`/`Esc` operation, reduced-motion support, viewport-safe
popups, and `DeviceSafeInsets`-aware root GUI. Known limitations: dropdowns
and the external color-picker asset are mouse-driven; drag-to-move has no
keyboard equivalent; Roblox exposes no OS screen-reader bridge, so icon
buttons expose names via attributes/tooltips instead.

## Changelog

- **5.9.4** — UI/UX & accessibility overhaul: keyboard-navigable command list
  with status bar, queued hover-aware notifications, accessible tooltips, UI
  scale / reduce motion / high contrast prefs, larger touch targets, and
  contrast fixes. No command changes.
- **5.9.3** — Removed Discord-related buttons & commands.
