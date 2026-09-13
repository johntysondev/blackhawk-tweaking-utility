<div align="center">

# BlackHawk

**One-click PC performance optimizer for Fortnite and competitive shooters.**

[![Website](https://img.shields.io/badge/Website-blackhawk.onrender.com-000000?style=for-the-badge&logo=googlechrome&logoColor=white)](https://blackhawk.onrender.com)
[![Download](https://img.shields.io/badge/Download-BlackHawk.exe-000000?style=for-the-badge&logo=windows&logoColor=white)](https://blackhawk.onrender.com#download)
[![License](https://img.shields.io/badge/License-Free-000000?style=for-the-badge)](#)

</div>

---

## What is BlackHawk

BlackHawk is a free, portable Windows utility that applies 24 proven performance tweaks to your PC. Every change is backed up and fully reversible. One click to optimize, one click to restore.

No ads. No account. No data collection. Just performance.

**[blackhawk.onrender.com](https://blackhawk.onrender.com)**

---

## Features

### One-Click Optimization
Hit "Recommended" and BlackHawk applies every safe tweak instantly. Game Mode, power plans, GPU priority, network profile, Fortnite config, NVIDIA profiles, legacy DX11 mode, display overclock, startup cleanup.

### 100% Reversible
Every tweak saves the original value before changing it. Hit Restore and your PC is exactly as it was. No registry residue, no orphaned backups.

### Fortnite-Specific Tweaks
- **Performance Config** -- No shadows, low effects, 240 FPS cap, fullscreen, mouse accel off
- **Legacy DX11 Mode** -- Writes `-d3d11` to Epic launcher for lowest input delay
- **NVIDIA Max-FPS Profile** -- Reflex ON, uncapped FPS, VSync off, fast launch flags
- **Exclusive Fullscreen** -- Sets the Windows compat flag for true exclusive fullscreen
- **Epic Launcher Cleanup** -- Removes Epic Games from your startup sequence

### System Tweaks
- **Game Mode & Game DVR** -- Enable Game Mode, disable Game DVR recording overhead
- **Visual FX Performance** -- Windows visual effects set to performance
- **Mouse Acceleration** -- Raw input, no acceleration
- **Ultimate Power Plan** -- Maximum performance power plan
- **Fullscreen Optimizations** -- Disable FSO for lower latency
- **GPU Priority & Scheduler** -- High GPU priority, hardware-accelerated GPU scheduling
- **Nagle Algorithm Off** -- Low-latency networking
- **USB Selective Suspend** -- Prevent USB power-saving from adding latency
- **Background Apps** -- Disable background app execution
- **Telemetry & Widgets** -- Disable Windows telemetry and widget service

### Display Overclock
Detects every refresh rate your monitor supports and pushes it to the max.

### CPU/GPU Scoring
Animated real-time scoring of your hardware. See where your bottleneck is and what tweaks matter most.

### Startup Killer
Enumerates every third-party app, shortcut, and scheduled task that launches with Windows. One toggle kills them all. Windows components are never touched.

---

## Profiles

| Profile | Tweaks | Description |
|---------|--------|-------------|
| **Essential** | 5 | Game Mode, Game DVR, Visual FX, Mouse Accel, Keyboard Filter. Zero risk. |
| **Recommended** | 18 | Everything in Essential plus power plan, GPU priority, network, telemetry, Fortnite config. Fully reversible. |
| **Aggressive** | 24 | Every available optimization. GPU scheduler, timer resolution, startup killer. Max performance. |

---

## Screenshots

Visit **[blackhawk.onrender.com](https://blackhawk.onrender.com)** for a full preview of the UI.

---

## Requirements

- Windows 10 or 11
- No installation required (portable .exe)
- Admin mode for some tweaks (prompted inside the app)

---

## Running from Source

```bash
# Install dependencies
pip install customtkinter psutil

# Run the app
python blackhawk_tweak.py
```

---

## Building the .exe

```bash
pip install pyinstaller
pyinstaller --onefile --windowed --icon hawk.ico --name BlackHawk blackhawk_tweak.py
```

The output will be in `dist/BlackHawk.exe`.

---

## Project Structure

```
BlackHawk/
  blackhawk_tweak.py    # Main UI (CustomTkinter)
  tweaks.py             # Core tweak engine (registry, Fortnite, display, scoring)
  hawk.ico              # App icon
  requirements.txt      # Dependencies
  website/              # Marketing site
    index.html
    style.css
    script.js
```

---

## How It Works

1. Every tweak backs up the original value to `blackhawk_tweak_backup.json`
2. Tweaks are applied via Windows registry edits, powercfg commands, config file writes, and process management
3. The Restore page lets you revert individual tweaks or all at once
4. No background services, no auto-start, no telemetry of any kind

---

## Website

**[blackhawk.onrender.com](https://blackhawk.onrender.com)**

Features, full tweak list, download, and profile breakdowns.

---

## Disclaimer

BlackHawk modifies Windows registry settings and system configurations. While every tweak is reversible and tested, use at your own discretion. BlackHawk is not affiliated with Epic Games, NVIDIA, or Microsoft.

---

## License

Free and open source. Do whatever you want with it.
