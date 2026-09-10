<p align="center">
  <img src=".github/assets/atoll-logo.png" alt="Halo logo" width="120">
</p>

<h1 align="center">Halo</h1>

<p align="center">A Dynamic Island-style notch experience for macOS.</p>

---

Halo turns the MacBook notch into a compact command surface for media, system insight, and everyday utilities. It stays out of the way until you need it, then expands with native SwiftUI animations.

## Features

**Live Activities** — Halo surfaces what's happening right now in the notch: media playback, Focus mode changes, screen recording and privacy indicators, download progress (beta), and battery/charging status.

**Music controls** — Full playback control for Apple Music, Spotify, Cider, and other players, with inline artwork previews and a live audio visualizer.

**Lock Screen Widgets** — Glanceable panels on the lock screen for now playing, timers, charging state, connected Bluetooth devices, and weather.

**System insight** — Lightweight monitoring for CPU (including per-core usage and temperature), GPU, memory, network, and disk activity.

**Productivity tools** — Built-in timers, clipboard history, a color picker, calendar previews, a file shelf, and a terminal tab.

**Gesture controls** — Two-finger swipe down to open the notch and up to close it. Horizontal swipes over the music pane skip tracks or seek ±10 seconds, with haptics and button animations matching tap interactions.

**Customization** — Configurable layouts, animation styles, hover behaviour, per-feature toggles, and remappable global shortcuts.

## Requirements

- **macOS 14.6 or later** (the app target's deployment minimum; optimised for macOS 15+)
- A MacBook with a notch — 14" or 16" MacBook Pro, Apple silicon
- **Xcode 16 or later** to build from source (Swift 5)
- Permissions granted as needed: Accessibility, Camera, Calendar, Screen Recording, and Music

## Installation

Build from source:

```bash
git clone https://github.com/umachinchula/halo.git
cd halo
open DynamicIsland.xcodeproj
```

Then in Xcode:

1. Select the **DynamicIsland** scheme.
2. Choose your Mac as the run destination.
3. Set your own development team under **Signing & Capabilities** if you plan to run a signed build.
4. Press **⌘R** to build and run.

On first launch, grant the permissions Halo requests — Accessibility and Screen Recording require quitting and relaunching the app before they take effect.

## Credits

**Halo is based on the open-source [Atoll](https://github.com/Ebullioscopic/Atoll) project by [Ebullioscopic](https://github.com/Ebullioscopic), licensed under GPL-3.0.**

Halo is an independent fork and is not affiliated with or endorsed by the Atoll project or its authors.

Atoll itself derives from [Boring.Notch](https://github.com/TheBoredTeam/boring.notch) by [TheBoredTeam](https://github.com/TheBoredTeam), also licensed under GPL-3.0.

This project additionally builds on, or adapts work from:

- [Alcove](https://tryalcove.com) — inspiration for the Minimalistic Mode interface and lock screen widget concepts
- [Stats](https://github.com/exelban/stats) — CPU temperature via SMC, frequency sampling through IOReport, per-core utilisation tracking
- [Open Meteo](https://open-meteo.com) — weather API for the lock screen widgets
- [SkyLightWindow](https://github.com/Lakr233/SkyLightWindow) — window rendering for lock screen widgets
- [rtaudio](https://github.com/ZephyrCodesStuff/rtaudio) — live music visualizer
- [SwiftTerm](https://github.com/migueldeicaza/SwiftTerm) — terminal tab in standard mode
- [DynamicNotch](https://github.com/jackson-storm/DynamicNotch) — battery HUDs
- Wick — iOS-style timer design for the lock screen widget, used with thanks to Nate
- [OpenUsage](https://github.com/robinebers/openusage) — LLM usage tracking
- [OpenRouter](https://openrouter.ai) — automated model pricing API

See [NOTICE](NOTICE) for additional attribution.

## License

Halo remains licensed under the **GNU General Public License v3.0**, inherited from Atoll. See [LICENSE](LICENSE) for the full terms.
