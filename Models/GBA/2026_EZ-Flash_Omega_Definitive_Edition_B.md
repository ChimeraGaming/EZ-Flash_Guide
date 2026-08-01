# EZ-Flash Omega Definitive Edition B (2026)

## Overview

The EZ-Flash Omega Definitive Edition B is a hardware-updated replacement for the original Omega Definitive Edition.

Not to be mistaken with the [2021 EZ-Flash Omega Definitive Edition](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Models/GBA/2021_EZ-Flash_Omega_Definitive_Edition.md), which had Version A and Version B hardware revisions.

## Firmware

[Official Firmware Download](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Definitive-Edition-B-Downloads.html)

---

## Key Features

- 512Mbit PSRAM
  - Directly loads GBA ROMs up to 64MB
- 960Mbit NOR flash
- Improved NOR management
  - Delete individual games without clearing later entries
  - Rewrite freed NOR space
  - View current NOR usage by pressing START
- FRAM save storage
  - Save data does not depend on the RTC battery
- Dual Mode A/B switch
  - Mode A: Standard GBA flashcart operation
  - Mode B: Standalone game, rumble, RAM expansion, and GBA-to-DS link features
- GBA and Nintendo DS rumble support
- GBA-to-DS game-link support
- Nintendo DS Browser RAM expansion support
- Real-Time Clock with a replaceable coin-cell battery
- Cheat support
- Soft reset
- Save states
- Sleep mode
- Customizable hotkeys
- GB, GBC, and NES support through built-in emulators
- microSD support from 4GB to 128GB
- FAT16, FAT32, and exFAT support
- Upgradeable kernel and firmware

---

## Notes

- Do not install firmware or kernel files made for the original Omega Definitive Edition
- The Definitive Edition B uses `ezbluekernel.bin`
- The original Omega Definitive Edition has been discontinued
- Released in 2026

---

## Compare Previous Omega DE

| Feature | 2021 Omega Definitive Edition | 2026 Omega Definitive Edition B |
| --- | --- | --- |
| PSRAM | 256Mbit / 32MB | 512Mbit / 64MB |
| Maximum direct-load ROM size | 256Mbit / 32MB | 512Mbit / 64MB |
| NOR flash | 512Mbit / 64MB | 960Mbit / 120MB |
| NOR game deletion | Games must be deleted from the last entry backward | Individual games can be deleted and the freed space reused |
| NOR usage display | Not available | Available by pressing `START` |
| Hardware revisions | Rev A and Rev B boards | Blue PCB marked `EZODE-B` |
| Kernel file | `ezkernelnew.bin` | `ezbluekernel.bin` |
| Firmware compatibility | Original Omega DE firmware and kernel only | Omega DE B firmware and kernel only |
| FRAM save storage | Yes | Yes |
| Mode A/B switch | Yes | Yes |
| GBA and DS rumble | Yes | Yes |
| DS RAM expansion | Yes | Yes |
| GBA-to-DS link support | Yes | Yes |
