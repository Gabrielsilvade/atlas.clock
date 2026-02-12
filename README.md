# Atlas Clock

![Banner Image](./banner-image.png)

**atlas.clock** is a fast, interactive terminal user interface (TUI) for tracking world timezones. Part of the **Atlas Suite**, it offers a clean, high-visibility dashboard with millisecond-precision real-time counters and a "local-first" philosophy.

![Go Version](https://img.shields.io/badge/Go-1.25+-00ADD8?style=flat&logo=go)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)

## ✨ Features

- 🌍 **Multi-Timezone Dashboard:** View multiple world clocks simultaneously in a responsive grid.
- ⏱️ **High-Precision Detail:** Deep-dive into any clock for a "boxy" ASCII real-time counter with millisecond precision.
- 🧭 **Easy Discovery:** Browse through a comprehensive list of ~400+ IANA timezones (Europe/Istanbul, America/New_York, etc.).
- ⌨️ **Vim-style Navigation:** Full 4-way grid navigation using `h/j/k/l` or arrow keys.
- 🛡️ **Safety First:** Multi-step confirmation for both adding and deleting clocks to prevent accidental changes.
- 💾 **Local Persistence:** Your dashboard configuration is saved locally in `~/.atlas/clock.json`.
- 📦 **Zero Dependencies:** Compiles to a single static binary for Windows, Linux, and macOS.

## 🚀 Installation

### From Source
```bash
git clone https://github.com/fezcode/atlas.clock
cd atlas.clock
gobake build
```
Binaries for all platforms will be generated in the `build/` directory.

## ⌨️ Usage

Simply run the binary to enter the dashboard:
```bash
./atlas.clock
```

### Adding a Clock
1. Press `a` to enter the **Add** flow.
2. Enter a **Label** for the clock (e.g., "Office", "Home", "Server").
3. Scroll through the **Timezone List** and press `Enter` to select.
4. Confirm the addition by pressing `y`.

### Deleting a Clock
1. Navigate to the clock you wish to remove.
2. Press `d`.
3. Confirm the deletion by pressing `y`.

## 🕹️ Controls

| Key | Action |
|-----|--------|
| `↑/↓` or `k/j` | Navigate Up/Down in grid |
| `←/→` or `h/l` | Navigate Left/Right in grid |
| `Enter` | Open high-precision detail view |
| `a` | Add a new world clock |
| `d` | Delete selected clock (requires confirmation) |
| `Esc` / `Backspace` | Back to List View / Cancel |
| `q` or `Ctrl+C` | Quit Atlas Clock |

## 📂 Storage Location

Your clock configuration is stored locally in your user's home directory:

- **Windows:** `%USERPROFILE%\.atlas\clock.json`
- **Linux/macOS:** `~/.atlas/clock.json`

## 🏗️ Building

This project uses **gobake** for orchestration. To build for your current platform or cross-compile for others:

```bash
# Build for all platforms
gobake build

# Clean build artifacts
gobake clean
```

## 📄 License
MIT License - see [LICENSE](LICENSE) for details.
