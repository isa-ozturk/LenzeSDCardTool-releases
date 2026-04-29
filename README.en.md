[![Lang TR](https://img.shields.io/badge/lang-Türkçe-red)](README.md)
[![Lang EN](https://img.shields.io/badge/lang-English-blue)](README.en.md)

<div align="center">

# Lenze SD Card Tool

**SD card management tool for Lenze licensed devices — cleaning, inspection, and configuration in a single application.**

[![Release](https://img.shields.io/github/v/release/isa-ozturk/LenzeSDCardTool-releases?style=flat-square&color=blue)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)
[![Platform](https://img.shields.io/badge/platform-Windows-lightgrey?style=flat-square)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)
[![Latest Downloads](https://img.shields.io/github/downloads/isa-ozturk/LenzeSDCardTool-releases/latest/total?style=flat-square&color=blue&label=latest%20downloads)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)
[![Total Downloads](https://img.shields.io/github/downloads/isa-ozturk/LenzeSDCardTool-releases/total?style=flat-square&color=green&label=total%20downloads)](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases)

[⬇️ Download Latest Version](https://github.com/isa-ozturk/LenzeSDCardTool-releases/releases/latest)

</div>

---

## What is this?

Lenze SD Card Tool is a Windows desktop application designed to manage SD cards used in Lenze PLC and HMI devices.

It provides a unified interface for:
- SD card cleaning  
- License (credit) status validation  
- Device IP configuration  
- Project and recipe inspection  

Supports both:
- **New Generation** (Linux-based, easyui / CODESYS — c5x0, c750, i950)  
- **Legacy Generation** (Windows CE, VisiWinNET — c300, p300, 3200C, p500)

Delivered as a **single EXE**, no installation required.

---

## Features

### Cleaning
- Smart SD card detection (ignores USB drives)
- License file protection
- Multi-threaded deletion engine
- Real-time progress tracking
- Optional safe eject after operation
- Cleaning history tracking

### SD Card Inspection
- Automatic generation detection
- 4-tab detailed view:
  - General (filesystem, usage, license status)
  - Device (model, firmware, IP, MAC, serial)
  - Projects
  - Recipes
- License validation and credit reading

### IP Configuration
- Modify IP, subnet, gateway directly via SD card
- Validation and auto gateway calculation
- Restore previous configuration (ip_old.txt)
- Supports both generations

### User Experience
- Modern Windows 11 styled UI
- Light / Dark theme
- Double-click to open in Explorer
- Context menu (Open, Info, IP, Eject)
- Auto update via GitHub

---

## System Requirements

| Requirement | Minimum |
|------------|--------|
| OS | Windows 10 (64-bit) |
| .NET | 4.7.2+ |
| RAM | 50 MB |
| Disk | 10 MB |
| Internet | Only for update check |

---

## Installation

No installation required.

1. Download `SDCardCleaner.exe` from Releases  
2. Place it anywhere  
3. Run it  

> Windows SmartScreen warning may appear → "More info → Run anyway"

---

## Usage

### Cleaning
1. Insert SD card  
2. Select from list  
3. Click **Clean**  
4. Confirm  

### View Info
- Click **Info** or right-click menu  
- Explore all device and SD card data  

### Configure IP
- Click **IP**  
- Enter new address  
- Save → written as `ip.txt`

---

## Supported Devices

| Generation | Platform | Devices |
|-----------|----------|--------|
| New | Linux / CODESYS | c5x0, c750, i950 |
| Legacy | Windows CE | c300, p300, 3200C, p500 |

---

## Updates

Application checks updates on startup.  
Manual check available via UI.

---

## License

Developed for internal use at **Lenze**.  
Source code is private.

---

<div align="center">
  <sub>Developed by <a href="https://github.com/isa-ozturk">isa-ozturk</a></sub>
</div>
