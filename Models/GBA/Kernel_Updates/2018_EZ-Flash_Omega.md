# EZ-Flash Omega Firmware and Kernel History

## Current Version

- Kernel: 1.10
- Firmware: 9.0
- Update file: `ezkernel.bin`

[Official Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Downloads.html)

[Official EZ-FLASH Downloads](https://www.ezflash.cn/download/)

[Official User Manual](https://www.ezflash.cn/omega.html)

---

## Update Instructions

1. Back up the `SAVER` folder from the microSD card.
2. Download and extract the latest official package.
3. Place `ezkernel.bin` in the root of the microSD card.
4. Insert the microSD card into the Omega.
5. Hold `R` while powering on the console.
6. Do not turn off the console during the kernel or firmware update.
7. Restart the console if prompted after the firmware update.
8. Confirm the installed versions in `System Setting`.

Only use `ezkernel.bin` made for the original EZ-Flash Omega.

---

## Version History

| Kernel | Firmware | Changes |
| --- | --- | --- |
| 1.10 | 9.0 | Updated the built-in GBC emulator to Jagoomba Color 0.5. Added addon support for Goodboy Galaxy 1.2. Updated FatFs to version 0.15. |
| 1.09 | 9.0 | Fixed the built-in Goomba emulator being unable to save. |
| 1.08 | 9.0 | Fixed known issues involving Dragon Ball Z anti-piracy and the Digi Communication 2 save system. |
| 1.08 | 8.0 | Fixed the long-standing random freezing problem. |
| 1.07 | 7.0 | Updated Goomba to the May 2019 release. Removed the emulator SRAM write action when exiting. |
| 1.06 | 7.0 | Fixed freezing under certain circumstances. |
| 1.05 | 6.0 | Added support for recently released iQue GBA ROMs. |
| 1.04 | 6.0 | Removed automatic battlefield saving from the Fire Emblem series. Added a save-states-only mode with customizable hotkeys and improved compatibility. |
| 1.03 | 5.0 | Refactored the firmware, reduced power consumption, added an option to disable the in-game RTC module, enabled NOR on original GBA systems, fixed an AGS-101 European save issue, and rewrote the addon patch engine. |
| 1.02 | 4.0 | Added automatic cheat-library matching and a recently played games list. |
| 1.01 | 3.0 | Improved compatibility with original GBA hardware and different microSD cards. Fixed soft-reset bugs. |
| 1.00 | 2.0 | Initial factory release. |

---

## Major Changes by Version

### Kernel 1.10

- Replaced the older GBC emulator with Jagoomba Color 0.5
- Added addon support for Goodboy Galaxy 1.2
- Updated the FatFs filesystem library to version 0.15

### Kernel 1.09

- Fixed save failures inside the built-in Goomba emulator

### Kernel 1.08 and Firmware 9

- Fixed anti-piracy problems affecting Dragon Ball Z games
- Fixed the Digi Communication 2 save issue

### Kernel 1.08 and Firmware 8

- Fixed a random freezing problem that had existed across several earlier releases

### Kernel 1.04

- Removed automatic battlefield saving from Fire Emblem games
- Added a separate save-state mode that does not load the full in-game menu
- Improved compatibility when only save states are enabled

### Kernel 1.03

- Rebuilt major portions of the firmware
- Reduced power consumption
- Added the option to disable the in-game RTC module
- Enabled NOR flash on original GBA hardware
- Rewrote the addon patch engine
- Fixed addon problems with games such as Lady Sia and Mario & Luigi

---

## Upgrade Warnings

- Never turn off the console during a kernel or firmware update.
- Use a console with a charged battery or a reliable external power source.
- Do not install firmware made for the Omega Definitive Edition, Definitive Edition B, or Air.
- Return to the official kernel before diagnosing problems caused by a custom kernel or theme.
- Back up the `SAVER` folder before updating.
- Do not interrupt NOR writing, deletion, or formatting.

---

## Known Version Issues

### Kernel 1.01 and Firmware 3

The official changelog listed these unresolved issues:

- NOR flash was not usable on an original GBA
- Final Fantasy Tactics could freeze while saving

NOR support on original GBA hardware was added in Kernel 1.03.

### Versions Before Kernel 1.08 and Firmware 8

Earlier versions could experience random freezing. Kernel 1.08 and Firmware 8 specifically addressed this long-standing problem.

### Fire Emblem Saving

Starting with Kernel 1.04, automatic battlefield saving was removed from the Fire Emblem series.

Use the game's manual battlefield save and chapter save points.

### Addon Compatibility

Cheats, save states, sleep mode, soft reset, and the in-game menu patch the game during loading. Some games and modified ROMs may require Clean Boot.

---

## Sources

- [Official EZ-Flash Omega Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Downloads.html)
- [Official EZ-FLASH Manufacturer Downloads](https://www.ezflash.cn/download/)
- [Official EZ-Flash Omega User Manual](https://www.ezflash.cn/omega.html)
