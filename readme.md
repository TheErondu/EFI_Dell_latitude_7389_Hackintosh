# Dell Latitude 7389 Hackintosh - OpenCore

OpenCore EFI configuration for Dell Latitude 7389 2-in-1 Convertible

![macOS Version](https://img.shields.io/badge/macOS-Sonoma%2014.x-blue)
![OpenCore Version](https://img.shields.io/badge/OpenCore-1.0.3-green)
![License](https://img.shields.io/badge/License-MIT-purple)

## 💻 Hardware Specifications

| Component      | Model                                    |
|----------------|------------------------------------------|
| **CPU**        | Intel Core i5-7200U (Kaby Lake)         |
| **GPU**        | Intel HD Graphics 620                    |
| **RAM**        | 8GB DDR4 2133MHz                        |
| **Storage**    | 256GB NVMe SSD                          |
| **Display**    | 13.3" FHD Touchscreen (1920x1080)      |
| **Audio**      | Realtek ALC3246                         |
| **WiFi/BT**    | Intel Wireless (replace recommended)    |
| **Ethernet**   | None (use USB adapter)                  |

## ✅ What Works

- [x] CPU Power Management
- [x] Intel HD 620 Graphics (full acceleration)
- [x] Audio (speakers, headphones, mic)
- [x] Touchscreen
- [x] Touchpad with gestures
- [x] All USB Ports
- [x] Battery status
- [x] Brightness control
- [x] Sleep/Wake/Hibernation
- [x] Camera
- [x] SD Card Reader
- [x] Keyboard & Function keys
- [x] HDMI output
- [x] WiFi (Intel - requires AirportItlwm)
- [x] Bluetooth (partial support)

## ❌ What Doesn't Work
- [ ] Ambient light sensor
- [ ] Tablet mode auto-rotation

## 🔧 BIOS Settings

### Disable
- Secure Boot
- Fast Boot
- Wake on LAN

### Enable
- AHCI Mode
- UEFI Boot Mode

## 📦 Installation

1. Create macOS Sonoma installer
2. Mount EFI partition
3. Copy this EFI folder
4. **Generate your own serials** with [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
   - SMBIOS: MacBookPro14,1
5. Install macOS

## 🛠️ Post-Installation

### Hibernation Setup
```bash
sudo pmset -a hibernatemode 25
sudo pmset -a lidwake 0
sudo pmset -a sleep 0
sudo pmset -a darkwakes 0
sudo pmset -a standby 0
```

## 📝 Kexts Used

- Lilu
- WhateverGreen
- AppleALC
- VirtualSMC
- VoodooPS2Controller
- VoodooI2C + VoodooI2CHID
- AirportItlwm
- IntelBluetoothFirmware
- USBMap (custom)
- RealtekCardReader

## 🤝 Credits

- [Acidanthera](https://github.com/acidanthera) - OpenCore & kexts
- [Dortania](https://dortania.github.io/) - Guides
- [OpenIntelWireless](https://github.com/OpenIntelWireless) - Intel WiFi/BT

## ⚠️ Disclaimer

Provided as-is. Educational purposes only. Generate your own serials!

## 🌟 Support

If this helped you, give it a ⭐!