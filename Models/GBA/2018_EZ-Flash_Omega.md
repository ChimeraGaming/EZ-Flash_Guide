# EZ-Flash Omega (2018)

## Overview

The EZ-Flash Omega is a GBA flashcart released in 2018. It loads standard GBA games from a microSD card into PSRAM and can permanently store selected games in NOR flash.

Not to be mistaken with the [2021 EZ-Flash Omega Definitive Edition](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Models/GBA/2021_EZ-Flash_Omega_Definitive_Edition.md), which added FRAM save storage, lower power consumption, rumble, and Nintendo DS expansion functions.

## Firmware

Latest official release:

- Kernel 1.10
- Firmware 9.0
- Kernel file: `ezkernel.bin`

[Official Firmware Download](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Downloads.html)

[Official User Manual](https://www.ezflashomega.com/pages/EZ-FLASH-Omega-User-Manual.html)

### Kernel 1.10 Changes

- Updated the built-in GBC emulator to Jagoomba Color 0.5
- Added addon support for Goodboy Galaxy version 1.2
- Updated the FatFs library to version 0.15

Kernel 1.08 and Firmware 8 fixed a long-standing random freezing issue. Older firmware should be updated before troubleshooting stability problems.

---

## Key Features

- 256Mbit / 32MB PSRAM
  - Quickly loads standard GBA games from the microSD card
- 512Mbit / 64MB NOR flash
  - Permanently stores selected games until they are deleted
  - Supports games too large for PSRAM
- Hardware-based save writing to microSD
- Automatic GBA save-type detection
- Real-Time Clock
- Cheat support
- Soft reset
- Save states
- Sleep mode
- Customizable hotkeys
- Recent-game list
- Game thumbnails
- Multiboot support
- GB, GBC, and NES playback through built-in emulators
- microSD support from 128MB to 128GB
- FAT16, FAT32, and exFAT support
- Upgradeable kernel and firmware

---

## Game Loading

### Clean Boot

Runs the game without cheats, soft reset, save states, sleep mode, or other addon patches.

Clean Boot should be used when troubleshooting compatibility problems.

### Boot With Addon

Runs the game with the features enabled under the system's `ADDON` settings.

Available addon features include:

- Cheats
- Soft reset
- Save states
- Sleep mode
- In-game menu

Addon features patch the game while it is loading and may not work correctly with every game or ROM hack.

### NOR Flash

Games can also be written to the cartridge's 512Mbit NOR flash.

NOR is useful for:

- Frequently played games
- Faster startup
- 64MB GBA Video ROMs
- Large homebrew that cannot fit in PSRAM

Games must normally be deleted from NOR in reverse order. The most recently written game must be deleted before games stored before it.

Formatting the entire NOR area takes approximately four minutes.

Do not turn off the console while NOR is being written, deleted, or formatted.

---

## Save Behavior

The Omega writes game save data directly to the microSD card.

After saving inside a game:

1. Leave the console powered on for at least two to three seconds.
2. Wait approximately five seconds when possible.
3. Do not immediately reset or turn off the console.

Turning off or resetting too quickly can interrupt the write process and corrupt the save file or microSD filesystem.

The RTC battery is not required to retain normal GBA save data. A dead RTC battery only affects time-based functions.

### GB, GBC, and NES Saves

GB, GBC, and NES games run through built-in emulators.

Before exiting an emulated game:

1. Press `L + R` to trigger the emulator's save process.
2. Select the exit option.
3. Wait several seconds before turning off the console.

Regularly back up the `SAVER` folder.

---

## File Structure

A typical official-kernel setup contains:

```text
/EZKERNEL.BIN
/IMGS/
/CHEAT/
/SAVER/
/RTS/
