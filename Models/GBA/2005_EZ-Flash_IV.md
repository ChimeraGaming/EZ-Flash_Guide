# EZ-Flash IV (2005)

## Overview

The EZ-Flash IV is a GBA flashcart introduced during the mid-2000s. It was the first long-running EZ-Flash GBA model to use removable storage for the ROM library while retaining PSRAM, NOR flash, and battery-backed SRAM inside the cartridge.

The standard full-size EZ-Flash IV was produced in multiple hardware revisions:

| Version | Storage | Notes |
| --- | --- | --- |
| Original white model | MiniSD | Requires a card no larger than 2GB formatted as FAT16 when installing a modern kernel |
| Later black model | microSD | Supports microSDHC cards up to 32GB with the current kernel |

This page covers the standard full-size EZ-Flash IV. The EZ-Flash IV Lite, Lite Compact, and Lite Deluxe are separate hardware variants with different capabilities.

The EZ-Flash IV was succeeded by the [2017 EZ-Flash Reform](./2017_EZ-Flash_Reform.md) and later replaced by the [2018 EZ-Flash Omega](./2018_EZ-Flash_Omega.md).

## Kernel

Latest official release:

- Kernel: 2.05
- Update file: `ezfla_up.bin`
- Recommended filesystem: FAT32
- Maximum officially supported storage: 32GB

[Official Kernel Download](https://www.ezflash.cn/download/)

[Official EZ-Flash IV Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)

### Updating the Kernel

1. Start the cartridge normally and allow any pending save backup to finish.
2. Back up the `SAVER` folder from the storage card.
3. Download and extract EZ4Kernel 2.05.
4. Place `ezfla_up.bin` in the root of the card.
5. Insert the card into the EZ-Flash IV.
6. Hold `R` while powering on the console.
7. Keep the console powered until the update finishes.
8. Confirm that version `2.05` appears in the menu.
9. Delete `ezfla_up.bin` after the update.

Do not turn off the console while the kernel is being installed.

### Original White MiniSD Model

The original white MiniSD model must be updated using:

- A MiniSD card no larger than 2GB
- FAT or FAT16 formatting

A microSD card inside a proper MiniSD adapter can also be used.

After Kernel 2.05 is installed, the official instructions allow switching back to a larger microSD card through an adapter.

---

## Key Features

- 128Mbit / 16MB PSRAM
- 256Mbit / 32MB NOR flash
- Battery-backed SRAM save storage
- microSDHC support up to 32GB on supported revisions
- Automatic ROM patching with Kernel 2.00 and newer
- Soft reset
- Sleep mode
- Configurable hotkeys through `KEYSET.CFG`
- Multiple games stored on one removable card
- Persistent NOR game storage
- GBA homebrew support
- Custom kernel skins
- Legacy cheat support through patched ROMs
- Upgradeable kernel
- GBA playback on:
  - Game Boy Advance
  - Game Boy Advance SP
  - Game Boy Micro
  - Nintendo DS through Slot-2
  - Nintendo DS Lite through Slot-2

---

## Game Loading

The EZ-Flash IV has two methods for loading GBA games.

| Loading Mode | Capacity | Behavior |
| --- | ---: | --- |
| PSRAM | Games up to 16MB | Loaded from the storage card whenever the game is launched |
| NOR flash | 32MB total | Slower initial write, but games remain installed after power is removed |

### PSRAM

Press `A` on a game to load it into PSRAM.

PSRAM is the standard loading method for games no larger than 16MB. Its contents are lost when the console is powered off, so the game must be loaded again during the next session.

Loading can take considerably longer than on newer EZ-Flash cartridges.

### NOR Flash

Press `SELECT` on a game to write it to NOR flash.

NOR flash is required for GBA games larger than 16MB. It can also be used for frequently played smaller games.

Games written to NOR remain installed after the console is powered off.

The combined size of all installed games cannot exceed 32MB. A single 32MB game will use the entire NOR area.

### NOR Management

- `A` launches a game stored in NOR
- `SELECT` deletes the most recently written game
- `START` formats the entire NOR area

Games normally must be deleted from the newest entry backward.

Do not turn off the console while NOR is being written, deleted, or formatted.

---

## Automatic ROM Patching

Kernel 2.00 introduced an onboard Auto Patch Engine.

With Kernel 2.00 or newer, clean GBA ROMs can be copied directly to the storage card. A desktop patching program is not required for normal commercial games.

When a game is launched for the first time, the kernel analyzes the ROM and creates the required patch data.

Generated patch files are stored in:

```text
/PATCH/
```

The initial launch may take longer while the patch is created. Later launches reuse the stored patch file.

Delete the corresponding file from the `PATCH` folder when:

- Replacing a ROM with another revision
- Applying a new ROM hack
- Updating a translation
- Changing the ROM without changing its filename
- Troubleshooting an incorrectly detected save type

The kernel will generate new patch data during the next launch.

### Older Kernels

Kernels before 2.00 normally require ROMs to be processed through the EZ4 Client before being copied to the storage card.

Kernel 2.05 is recommended for normal GBA use because it performs this patching directly on the cartridge.

---

## Save Behavior

The EZ-Flash IV does not write saves directly to the storage card during gameplay.

Game save data is initially stored in the cartridge's battery-backed SRAM. The kernel copies that data to the matching file in the `SAVER` folder the next time the EZ-Flash IV menu starts.

### Proper Save Procedure

1. Save normally inside the game.
2. Soft reset to the EZ-Flash menu or power off the console.
3. Start the console again with the EZ-Flash IV inserted.
4. Allow the save-backup process to finish.
5. Do not press `L` while the backup is running.
6. Wait for the menu to finish loading before powering off again.

Save files are stored in:

```text
/SAVER/
```

The ROM and save file must use matching filenames.

Example:

```text
Pokemon Emerald.gba
Pokemon Emerald.sav
```

Only one active save is held in SRAM at a time. Loading another game before the previous save has been backed up can overwrite the unbacked save data.

Regularly copy the entire `SAVER` folder to another device.

### Save Battery

The internal battery retains SRAM data while the console is powered off.

A weak or dead battery can cause:

- Loss of the most recent unbacked save
- Language selection appearing during every startup
- A low-SRAM-battery warning
- Corrupted menu text or graphics
- Settings failing to remain saved

Most original EZ-Flash IV boards use a soldered battery. Replacing it generally requires soldering.

The battery does not provide Real-Time Clock functionality.

---

## Soft Reset and Sleep Mode

Kernel 2.02 introduced Global Soft Reset and Sleep, also called GSS.

Default controls:

| Function | Default Hotkey |
| --- | --- |
| Return to the EZ-Flash menu | `L + Up + B` |
| Enter sleep mode | `L + R + Start` |
| Wake from sleep | `Start + Select` |

Hotkeys can be changed through `KEYSET.CFG` in the root of the storage card.

### Game-Loading Controls

| Control | Function |
| --- | --- |
| `A` | Load normally |
| `L + A` | Load using hard reset |
| `L + B` | Load without GSS |
| `SELECT` | Write to NOR |
| `L + SELECT` | Write to NOR without GSS |

Some games do not work correctly when GSS is applied. Launch the affected game with `L + B` to disable soft reset and sleep for that session.

---

## Cheats

The EZ-Flash IV does not have the modern interactive cheat browser found on the Omega series.

Cheats can be used through older EZ4 Client workflows or ROMs that have been patched with a compatible trainer or cheat system.

Cheat-patched games may have lower compatibility than clean ROMs. Test the original ROM without cheats when troubleshooting freezes, save failures, or incorrect behavior.

---

## Themes

The EZ-Flash IV supports custom kernel skins.

Themes are compiled into a modified copy of:

`ezfla_up.bin`

They are not selected from a separate theme folder.

Installing a themed kernel replaces the currently installed kernel. Before installing one:

- Confirm that it is based on EZ4Kernel 2.05
- Confirm that it supports your EZ-Flash IV revision
- Back up the `SAVER` folder
- Keep a copy of the official Kernel 2.05 installer

Older themes may reinstall an older kernel and remove automatic patching, GSS improvements, or compatibility fixes.

Return to the official kernel before troubleshooting hardware, save, or game-loading problems.

---

## Legacy Nintendo DS Features

The EZ-Flash IV can be inserted into the Slot-2 GBA cartridge slot of an original Nintendo DS or Nintendo DS Lite.

When using the current kernel, its primary purpose is running GBA software through Slot-2.

Earlier EZ-Flash IV hardware and software revisions also advertised features such as:

- Nintendo DS mode
- Slot-2 memory expansion
- Nintendo DS Browser compatibility
- Nintendo DS homebrew loading

These features depended on older kernels, PassMe or FlashMe configurations, and other discontinued Nintendo DS software.

The EZ-Flash IV is not a Slot-1 Nintendo DS flashcart and should not be purchased primarily for Nintendo DS game playback.

---

## Recommended File Structure

```text
/
|-- ezfla_up.bin
|-- KEYSET.CFG
|-- GBA/
|   |-- Game 1.gba
|   \-- Game 2.gba
|-- PATCH/
\-- SAVER/
```

- `ezfla_up.bin` is only required while installing a kernel
- `KEYSET.CFG` contains optional GSS and hotkey settings
- `GBA` contains ROM files
- `PATCH` contains automatically generated ROM patches
- `SAVER` contains game save files

The `PATCH` and `SAVER` folders may be created automatically.

Delete `ezfla_up.bin` after successfully updating the kernel.

---

## Limitations

- No Real-Time Clock
- No save states
- No direct save writing to the storage card
- Battery power is required to retain an unbacked save
- Only 16MB of PSRAM
- Games larger than 16MB must be written to NOR
- NOR capacity is limited to 32MB
- NOR games must normally be deleted in reverse order
- PSRAM and NOR writing are slow compared with newer cartridges
- No modern in-cartridge cheat browser
- Soft-reset and sleep patches are incompatible with some games
- ROM hacks may not be detected correctly by the Auto Patch Engine
- Original MiniSD hardware can be sensitive to card adapters
- Most original batteries require soldering to replace
- No built-in RTC support for Pokémon time-based events
- Discontinued and no longer receiving kernel updates

---

## Known Problems

### No Nintendo Logo

This usually indicates poor contact between the cartridge and console.

- Remove and reinsert the cartridge
- Clean the cartridge contacts
- Check that the shell is assembled correctly
- Test the cartridge in another console

### Black Screen After the Nintendo Logo

The official troubleshooting information identifies this as a possible hardware failure.

Test another storage card and console. Persistent black screens may indicate that the cartridge requires repair or replacement.

### White Screen or Crash After Writing to PSRAM

A white screen or crash after a successful PSRAM write can indicate defective PSRAM.

Test several verified clean ROMs and another storage card. Persistent failures across multiple games can indicate failing cartridge hardware.

### `PSRAM Is Not Enough`

The selected game is larger than the cartridge's 16MB PSRAM.

Write the game to NOR by pressing `SELECT`.

### `NOR Space Is Not Enough`

The NOR area does not have enough free space.

Delete the most recently written games or format NOR before writing the new game.

A 32MB game requires the entire NOR area.

### `FAT Initial 0`

The storage card was not detected correctly.

- Remove and reinsert the card
- Clean its contacts
- Confirm that it is formatted correctly
- Test another card or adapter

### `FAT Initial 1`

The `ezfla_up.bin` file is incorrect, damaged, or intended for another cartridge.

Download a clean copy of EZ4Kernel 2.05 from the official EZ-Flash website.

### Empty File Browser

If the menu loads but no files appear:

- Confirm that the card is FAT32
- Reinsert the card
- Test another card
- Test another MiniSD adapter
- Move ROMs closer to the root directory
- Divide large libraries into multiple folders

### Language Selection Appears at Every Startup

This normally indicates that the internal battery is weak or dead.

Replace the battery and allow the cartridge to complete a normal startup.

### Corrupted Menu Graphics or Text

Glitched graphics or text can be caused by a weak battery or corrupted kernel installation.

1. Check or replace the battery.
2. Install the official Kernel 2.05.
3. Test another storage card.
4. Clean the cartridge contacts.

### Save Loss

Save loss can occur when:

- The battery is dead
- The boot-time save backup is skipped
- Another game is started before the backup finishes
- The ROM and save filenames do not match
- The storage card is removed during a write
- The `SAVER` folder is damaged
- An incorrect patch file is being used

### GSS Freezing

Some games freeze or produce graphical or audio problems with GSS enabled.

Launch the game with:

`L + B`

This disables soft reset and sleep for that launch.

### ROM Hacks and Translations

Modified ROMs may use unusual save types, expanded ROM sizes, or altered game code that the Auto Patch Engine does not recognize.

Possible symptoms include:

- White screens
- Freezing
- Saves not being created
- Saves loading incorrectly
- GSS failing
- The game working once and failing after modification

Delete the corresponding file from the `PATCH` folder and allow the kernel to process the ROM again.

If the problem continues:

- Disable GSS
- Try hard-reset loading with `L + A`
- Test the clean base ROM
- Use a manually save-patched version when required by the ROM hack

### MiniSD Adapter Problems

The original white model may behave unpredictably with poor-quality MiniSD-to-microSD adapters.

Possible symptoms include:

- Storage card not detected
- Intermittent file-browser failures
- Kernel updates freezing
- Save files becoming corrupted
- Games disappearing from the menu

Test a genuine MiniSD card or another high-quality adapter before assuming the cartridge has failed.

---

## Basic Troubleshooting

1. Allow any pending save backup to finish.
2. Back up the `SAVER` folder.
3. Install official EZ4Kernel 2.05.
4. Use a reputable card no larger than 32GB.
5. Format the card as FAT32.
6. Use a card no larger than 2GB formatted as FAT16 when updating the original white MiniSD model.
7. Remove old patch files from the `PATCH` folder.
8. Test with a verified clean GBA ROM.
9. Launch the game with `L + B` to disable GSS.
10. Try `L + A` for hard-reset loading.
11. Write games larger than 16MB to NOR.
12. Check or replace the internal battery if saves or settings disappear.
13. Test another storage card or MiniSD adapter.
14. Clean the cartridge contacts.
15. Test the cartridge in another console.

Persistent PSRAM failures, black screens, or crashes across multiple cards and consoles may indicate defective cartridge hardware.

---

## Notes

- Introduced during the mid-2000s
- Latest official kernel is 2.05
- Uses `ezfla_up.bin`
- Kernel 2.00 removed the need to patch normal ROMs on a computer
- Kernel 2.02 added Global Soft Reset and Sleep
- Kernel 2.03 added global and per-game GSS controls
- Kernel 2.04 added EZ-Flash Reform compatibility
- Uses 16MB PSRAM and 32MB NOR flash
- Uses battery-backed SRAM for pending save data
- Has no Real-Time Clock
- Original white models use MiniSD
- Later black models use microSD
- Replaced by the EZ-Flash Reform and EZ-Flash Omega
- Keep regular backups of the `SAVER` folder

---

## Sources

- [Official EZ-Flash IV Product Page](https://www.ezflash.cn/product/ez-flash-iv/)
- [Official EZ-Flash Downloads](https://www.ezflash.cn/download/)
- [Official EZ-Flash IV Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)
- [Kernel 2.00 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-00-released/)
- [Kernel 2.02 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-02-released/)
- [Kernel 2.03 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-03-released/)
- [Kernel 2.04 Announcement](https://www.ezflash.cn/ez4kernel-2-04-released/)

---

*Contribute corrections or additional findings through [GitHub Issues](https://github.com/ChimeraGaming/EZ-Flash_Guide/issues).*
