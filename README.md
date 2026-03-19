# Key Viewer — Geode Mod for GD 2.2074

A fully customizable on-screen key display overlay for Geometry Dash.

## Features

- 🎮 Shows which keys you're pressing in real-time during gameplay
- 🎨 Customize **idle color** and **pressed color** per your taste
- 🔲 Adjustable **opacity / transparency** (0–100%)
- 📍 Set the overlay **X/Y position** on screen (% of screen size)
- 📏 Adjustable **key box size**
- ⌨️ Remap all tracked keys (P1 Jump, P1 Left, P1 Right, P2 Jump) in settings
- 👁️ Optional display in the **Level Editor**

## Settings Reference

| Setting | Type | Default | Description |
|---|---|---|---|
| `opacity` | int 0–100 | 70 | Transparency of the overlay |
| `idle-color` | color | Dark gray | Key color when not pressed |
| `pressed-color` | color | Yellow | Key color when pressed |
| `key-p1-jump` | string | `Space` | P1 jump key name |
| `key-p1-left` | string | `A` | P1 left key name |
| `key-p1-right` | string | `D` | P1 right key name |
| `key-p2-jump` | string | `Up` | P2 jump key name |
| `overlay-x` | int 0–100 | 5 | Horizontal position (%) |
| `overlay-y` | int 0–100 | 10 | Vertical position (%) |
| `key-size` | int 20–100 | 40 | Box size in pixels |
| `show-in-editor` | bool | false | Show overlay in editor |

### Supported Key Names

Use these exact strings in the key settings:

```
A–Z, 0–9         (single character)
Space            (spacebar)
Up / Down / Left / Right
Shift / LShift / RShift
Ctrl
Alt
Enter
Tab
```

## Building

### Prerequisites
- [Geode SDK](https://geode-sdk.org) installed and `GEODE_SDK` env var set
- CMake 3.21+
- Visual Studio 2022 (Windows) / Xcode (macOS) / NDK (Android)

### Local Build

```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --config Release
```

The `.geode` file will be placed in `build/`.

### GitHub Actions (CI/CD)

Push to `main` → builds automatically for Windows, macOS, Android32, Android64.

Push a tag like `v1.0.0` → auto-creates a GitHub Release with all `.geode` files attached.

## Mod ID

`yourname.keyviewer` — replace `yourname` with your Geode username in `mod.json` and `CMakeLists.txt`.

## License

MIT
