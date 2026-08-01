# EZ-Flash Air (2025)

## Overview

The EZ-Flash Air is a budget GBA flashcart released on July 17, 2025 as the replacement for the original EZ-Flash Omega.

Unlike the Omega, the Air has no PSRAM. Games are stored on a microSD card but must be written to its 960Mbit NOR flash before they can be played.

## Firmware

Latest update:

- Firmware 4
- Kernel 1.05
- Kernel file: `ezairkernel.bin`

[Official Firmware Download](https://www.ezflashomega.com/pages/EZ-Flash-Air-Downloads.html)

[Official User Manual](https://www.ezflash.cn/air.pdf)

### Firmware 4 / Kernel 1.05 Changes

- Games can be individually deleted from NOR
- Freed NOR space can be reused
- NOR usage can be checked from the menu
- Improved ROM writing and reading compatibility

After updating, completely format or erase the existing NOR contents before writing games again.

---

## Key Features

- 960Mbit / 120MB NOR flash
- Writes a 256Mbit / 32MB game in approximately two minutes
- microSD support up to 128GB
- Battery-backed SRAM save storage
- Replaceable CR1220 battery for SRAM and RTC
- Real-Time Clock support
- Cheat support
- Soft reset
- Built-in rumble
- Nintendo DS Rumble Pak mode
- GBA-to-DS link support
- Standalone cartridge mode
- GB, GBC, and NES emulation
- Upgradeable kernel and firmware
- Compatible with Omega Definitive Edition replacement shells

---

## Operating Modes

### Mode A

Mode A provides access to the Air menu, microSD card, NOR library, cheats, save management, and settings.

### Mode B

Mode B can be configured for:

- Standalone and GBA-to-DS Link mode
- Nintendo DS Rumble Pak mode

Standalone and Link mode use the first compatible game stored in NOR.

The Air does not support Nintendo DS Browser RAM expansion.

---

## Save Behavior

Game saves are initially held in the cartridge's battery-backed SRAM.

The save is backed up to the microSD card when the Air menu performs its save-backup process. Addon Reset can also be used to return to the menu and back up the current save without turning the console off.

Before changing games or switching to Mode B:

1. Return to the Air menu or restart the console.
2. Allow the save-backup process to finish.
3. Confirm the save has been written before continuing.

Switching modes before the current save is backed up can cause the SRAM data to be overwritten.

A dead or poorly connected CR1220 battery can cause the current unbacked save and RTC settings to be lost.

Regularly back up the `SAVER` folder.

---

## Limitations

- No PSRAM or direct game loading from microSD
- Games must be written to NOR before use
- NOR capacity is limited to 120MB
- No GBA save states or sleep-mode patch
- No Nintendo DS RAM expansion
- Higher power consumption than several other GBA flashcarts
- Full-size shell protrudes from a Nintendo DS Lite
- GB, GBC, and NES games use emulation and may have compatibility or graphical issues
- Existing Omega and Omega Definitive Edition themes are not compatible
- Air theme support is currently experimental

---

## Reported Problems

The following problems have been reported by some users but do not affect every cartridge:

- Saves failing to back up automatically
- Saves only backing up when Addon Reset is used
- RTC settings resetting despite battery replacement
- White screens, graphical corruption, or freezing after writing games to NOR
- ROMs becoming corrupted during the NOR-writing process
- microSD cards intermittently failing to initialize
- CRC or checksum errors during firmware updates
- Cartridge no longer being detected after a crash
- Rumble remaining continuously active while the cartridge is not detected

Repeated corrupted NOR writes, graphical corruption across several games, or failure in multiple consoles usually indicates a defective cartridge.

Do not leave the cartridge powered if its rumble motor remains continuously active.

---

## Basic Troubleshooting

1. Install the latest Air-specific firmware and kernel.
2. Completely erase or format NOR after updating to Firmware 4 / Kernel 1.05.
3. Reformat the microSD card using the official recommendations.
4. Test with a different high-quality microSD card.
5. Use shorter ROM filenames if files are not detected.
6. Remove read-only attributes from ROM files and folders.
7. Clean the cartridge contacts with high-percentage isopropyl alcohol.
8. Test the cartridge in another console.

Do not install Omega or Omega Definitive Edition firmware on the Air.

---

## Notes

- Released July 17, 2025
- Replaced the standard EZ-Flash Omega
- Designed as a lower-cost alternative to the Omega Definitive Edition
- May not operate correctly with GBAccelerator speed settings other than 1x
- Keep a
