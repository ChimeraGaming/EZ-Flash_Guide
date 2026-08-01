# EZ-Flash Omega Definitive Edition (2021)

## Overview

The EZ-Flash Omega Definitive Edition is an upgraded version of the original EZ-Flash Omega, released in 2021.

It adds FRAM save storage, lower power consumption, built-in rumble, RGB lighting, and several Nintendo DS Slot-2 functions.

The original Definitive Edition was produced as Rev A and Rev B. These are hardware revisions of the same model with the same main features.

Not to be mistaken with the [2026 EZ-Flash Omega Definitive Edition B](./2026_EZ-Flash_Omega_Definitive_Edition_B.md), which is a separate model with different firmware and upgraded memory.

## Firmware

Latest official release:

- Kernel 1.06
- Firmware package 7.0
- Kernel file: `ezkernelnew.bin`
- Compatible with Rev A and Rev B

The package installs different firmware depending on the hardware revision:

- Rev A: Firmware 5
- Rev B: Firmware 7

[Official Firmware Download](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Definitive-Edition-Downloads.html)

[Official User Manual](https://www.ezflash.cn/omegade-en.pdf)

### Recent Firmware Changes

- Added support for Rev B units using S98 chips with a `020` suffix
- Updated the built-in GBC emulator to Jagoomba Color 0.5
- Fixed graphical corruption and freezing on a small number of Rev B units
- Fixed EEPROM save problems on units using certain S71 chips
- Improved stability and reduced random freezing on some consoles

---

## Key Features

- 256Mbit / 32MB PSRAM
  - Loads standard GBA games directly from the microSD card
- 512Mbit / 64MB NOR flash
  - Permanently stores selected games until they are deleted
- FRAM save storage
  - Active save data does not depend on the RTC battery
- Replaceable CR1025 battery
  - Used only for the Real-Time Clock
- Dual Mode A/B switch
- Built-in GBA and Nintendo DS rumble
- GBA-to-DS link support
- Nintendo DS Rumble Pak support
- Nintendo DS Memory Expansion Pak support
- Nintendo DS Browser RAM expansion support
- Configurable RGB breathing and SD-activity lights
- Real-Time Clock
- Cheat support
- Soft reset
- Save states
- Sleep-mode patch
- Customizable hotkeys
- GB, GBC, and NES emulation
- microSD support from 4GB to 128GB
- FAT32 and exFAT support
- Upgradeable kernel and firmware

---

## Operating Modes

### Mode A

Mode A provides normal flashcart operation, including:

- microSD game library
- PSRAM game loading
- NOR game management
- Save management
- Cheats
- Save states
- Sleep mode
- Emulator support
- Theme and system settings

Mode B must be configured from the settings menu while the cartridge is in Mode A.

### Mode B

Mode B can be configured for one of three functions.

#### Link

- Boots the first game stored in NOR as a standalone cartridge
- Supports compatible GBA-to-DS link features
- Supports Pokémon migration and other Slot-2 game detection
- Can boot without loading the EZ-Flash menu

#### Rumble

- Makes the cartridge function as a Nintendo DS Rumble Pak
- Works with Nintendo DS games that support the official Rumble Pak

#### RAM

- Makes the cartridge function as a Nintendo DS Memory Expansion Pak
- Supports the Nintendo DS Browser and compatible homebrew software

---

## Save Behavior

Game save data is stored in the cartridge's FRAM before being backed up to the microSD card.

The CR1025 battery is not required to retain game saves. A dead battery only affects the Real-Time Clock.

### Mode A Saves

When the kernel starts, it can automatically back up the most recently played game's FRAM data to the matching file in the `SAVER` folder.

Allow the save-backup process and SD activity light to finish before powering off or removing the microSD card.

Regularly back up the `SAVER` folder to another device.

### Mode B Link Saves

Mode B Link does not automatically load or back up the matching save file.

Before using Mode B Link:

1. Open the NOR menu in Mode A.
2. Select the first game stored in NOR.
3. Use `LOAD SAVE FILE` to copy its matching save from the `SAVER` folder into FRAM.
4. Turn off the console and switch to Mode B.
5. Play and save normally.

After playing:

1. Turn off the console and switch back to Mode A.
2. Open the NOR menu.
3. Select the same game.
4. Use `SAVE SAV FILE` to copy the save from FRAM back to the `SAVER` folder.

Loading or backing up the wrong game's save can overwrite valid save data.

---

## NOR Flash Behavior

Games written to NOR remain installed after the console is powered off.

The original Definitive Edition has limited NOR management:

- Games must normally be deleted in reverse order
- The most recently written game must be deleted first
- Removing an older game may require deleting every game written after it
- The entire NOR area can be formatted when necessary
- Mode B Link uses the first game stored in NOR

The 2026 Definitive Edition B improves this by allowing individual games to be deleted and the freed space to be reused.

---

## Themes and Custom Kernels

The original Omega Definitive Edition supports custom themes and custom kernels.

Popular options include:

- SimpleDE
- DS Style
- Custom `.skn` themes

Use versions specifically built for the original Omega Definitive Edition.

Do not install:

- Standard Omega firmware using `ezkernel.bin`
- Omega Definitive Edition B firmware using `ezbluekernel.bin`
- Air firmware using `ezairkernel.bin`

The original Definitive Edition uses `ezkernelnew.bin`.

Test the official kernel before troubleshooting problems involving a custom theme or kernel.

---

## Limitations

- PSRAM is limited to 256Mbit / 32MB
- NOR capacity is limited to 512Mbit / 64MB
- NOR games cannot be freely deleted in any order
- Mode B Link save files require manual loading and backup
- Mode B Link only boots the first game stored in NOR
- GB, GBC, and NES games run through emulation
- Emulator compatibility and save behavior are not perfect for every game
- Save states, cheats, soft reset, and sleep mode patch the game and may reduce compatibility
- The full-size cartridge protrudes from a Nintendo DS Lite
- RTC failure may not display a clear battery warning
- Analogue Pocket compatibility, especially Mode B, can depend on the Pocket firmware version

---

## Known Firmware Issues

Older firmware versions had several documented problems:

- Random freezing on some consoles
- Graphical corruption or freezing on a small batch of Rev B cartridges
- EEPROM saves not working correctly with certain S71 chips
- Compatibility problems with some S98 chips
- NOR games failing to write or appear correctly

Install the latest official kernel and firmware before troubleshooting these problems.

After upgrading to the newer Jagoomba Color emulator, previously played GBC games may load with incorrect compatibility settings.

Open the emulator settings with `L + R` and set:

`Prefer GBC over SGB`

---

## Reported Community Problems

The following problems have been reported by some users but do not affect every cartridge:

- NOR writing completes but the game does not appear
- Save files fail to back up or produce a read-save error
- White screens or freezing with certain ROM hacks
- Custom kernels or themes freezing during startup
- Mode B failing to boot on some Analogue Pocket firmware versions
- RTC resetting after the console is powered off
- microSD cards intermittently failing to initialize
- Cartridge detection problems caused by dirty or worn contacts

Persistent NOR failures, graphical corruption, or freezing across multiple consoles and microSD cards may indicate defective hardware.

---

## Basic Troubleshooting

1. Confirm whether the cartridge is Rev A or Rev B.
2. Install the latest official `ezkernelnew.bin`.
3. Test with the official kernel before using a custom theme.
4. Reformat the microSD card as FAT32 or exFAT.
5. Test with another high-quality microSD card.
6. Clean the cartridge contacts with high-percentage isopropyl alcohol.
7. Test the cartridge in another GBA-compatible console.
8. Disable cheats, save states, sleep mode, and soft reset when testing a problem game.
9. Use a clean ROM before testing ROM hacks or translations.
10. Follow the manual Mode B save procedure before assuming the save system has failed.

Do not turn off the console while the SD activity light is active.

---

## Notes

- Released in 2021
- Rev A and Rev B have the same main features
- Rev A and Rev B use different internal components and firmware versions
- Rev B is not the same product as the 2026 Definitive Edition B
- The CR1025 battery powers only the Real-Time Clock
- FRAM retains active save data without battery power
- Keep regular backups of the `SAVER` folder
