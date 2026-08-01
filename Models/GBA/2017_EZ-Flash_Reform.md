# EZ-Flash Reform (2017)

## Overview

The EZ-Flash Reform is a GBA flashcart released in late 2017 as the successor to the EZ-Flash IV.

Its primary improvement was a smaller circuit board that could be installed in either a standard GBA cartridge shell or a shorter Nintendo DS Lite shell. Internally, it operates similarly to the EZ-Flash IV and uses the same EZ4Kernel software.

The Reform was discontinued after the release of the [2018 EZ-Flash Omega](./2018_EZ-Flash_Omega.md).

## Kernel

Latest official release:

- Kernel: 2.05
- Update file: `ezfla_up.bin`

[Official Kernel Download](https://www.ezflash.cn/download/)

[Official EZ4 and Reform Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)

### Updating the Kernel

1. Back up the `SAVER` folder from the microSD card.
2. Download and extract the official EZ4 Kernel 2.05 package.
3. Place `ezfla_up.bin` in the root of the microSD card.
4. Insert the microSD card into the Reform.
5. Hold `R` while powering on the console.
6. Keep the console powered until the update finishes.
7. Confirm that version 2.05 appears in the upper-right corner of the menu.
8. Delete `ezfla_up.bin` from the microSD card after the update.

Do not install Omega, Omega Definitive Edition, Air, or other EZ-Flash kernels on the Reform.

---

## Key Features

- microSDHC support up to 32GB
- FAT32 filesystem support
- Automatic ROM patching through the Auto Patch Engine
- Battery-backed SRAM save storage
- Replaceable CR1220 battery
- Soft reset
- Sleep mode
- Configurable hotkeys through `KEYSET.CFG`
- Multiple games stored on one microSD card
- Persistent NOR game storage
- Custom kernel skins
- Swappable GBA and Nintendo DS Lite shells
- Upgradeable kernel

---

## Game Loading

The Reform has two methods for loading GBA games.

| Loading Mode | Capacity | Behavior |
| --- | ---: | --- |
| PSRAM | Games up to 16MB | Loads from the microSD card each time the game is launched |
| NOR Flash | 32MB total | Takes longer to write, but games remain installed after power is removed |

### PSRAM Mode

Press `A` on a game to load it into PSRAM.

PSRAM provides the normal loading method for games up to 16MB. Its contents are lost when the console is powered off, so the game must be loaded again the next time it is played.

### NOR Flash Mode

Press `SELECT` on a game to write it to NOR flash.

NOR is required for games larger than 16MB and can also be used for frequently played smaller games.

Games written to NOR remain installed after the console is powered off. Multiple games can be stored as long as their combined size does not exceed 32MB.

NOR games must be removed from the newest entry backward:

- `SELECT` deletes the last game written
- `START` formats the entire NOR area

Do not turn off the console while writing, deleting, or formatting NOR flash.

---

## Automatic ROM Patching

EZ4Kernel 2.00 and later include an Auto Patch Engine.

Clean GBA ROMs can be copied directly to the microSD card. The kernel automatically applies the required save patch when a game is launched for the first time.

Generated patch data is stored in:

```text
/PATCH/
```

The first launch may take considerably longer while the patch is created. Later launches use the stored patch file and load more quickly.

When replacing a ROM with a newer revision or a differently patched ROM hack, delete its existing file from the `PATCH` folder so the kernel can create a new patch.

---

## Save Behavior

The Reform does not write game saves directly to the microSD card during gameplay.

Save data is first stored in the cartridge's battery-backed SRAM. The kernel copies that SRAM data to the matching file in the `SAVER` folder the next time the Reform menu starts.

### Proper Save Procedure

1. Save normally inside the game.
2. Soft reset to the Reform menu or power the console off.
3. Restart the console with the Reform inserted.
4. Allow the save-backup process to finish.
5. Do not press `L` to skip the backup.
6. Confirm that the menu has fully loaded before turning the console off again.

Save files are stored in:

```text
/SAVER/
```

Only the current SRAM save is waiting to be backed up. Loading another game before the backup finishes can overwrite the unbacked save.

Regularly copy the entire `SAVER` folder to another device.

### CR1220 Battery

The replaceable CR1220 battery preserves:

- SRAM save data before it is backed up
- Language and menu settings

The Reform does not have a Real-Time Clock. The battery is not used for RTC functions.

A weak, missing, or poorly connected battery can cause:

- Loss of the current unbacked save
- Language selection appearing at every startup
- Corrupted menu text or graphics
- Unstable menu behavior

---

## Soft Reset and Sleep Mode

EZ4Kernel 2.02 and later support Global Soft Reset and Sleep, also called GSS.

Default controls:

| Function | Default Hotkey |
| --- | --- |
| Return to Reform menu | `L + Up + B` |
| Enter sleep mode | `L + R + Start` |
| Wake from sleep | `Start + Select` |

Hotkeys can be changed through the `KEYSET.CFG` file placed in the root of the microSD card.

Some games do not work correctly when the GSS patch is applied. Launch the affected game with `L + B` to bypass the soft-reset and sleep patch.

A hard boot can also be triggered with `L + A` for games with anti-piracy checks or other compatibility problems.

---

## Themes

The Reform supports custom EZ4Kernel skins.

Themes are compiled directly into a modified `ezfla_up.bin` file. They are not loaded from a separate `THEMES` folder.

Use a skin specifically built for EZ4Kernel 2.05. Installing an older or incompatible kernel skin can remove newer compatibility fixes or prevent the Reform from starting correctly.

Return to the official Kernel 2.05 before troubleshooting hardware, save, or game-loading problems.

---

## Limitations

- No Real-Time Clock
- No save states
- No Omega-style interactive cheat menu
  - Trainer-patched ROMs can still be used
- No built-in GB, GBC, or NES emulator menu
- No direct save writing to the microSD card
- Battery power is required to retain unbacked SRAM data
- Games larger than 16MB must be written to NOR
- NOR capacity is limited to 32MB
- NOR games must be deleted in reverse order
- Initial launches can be slow while automatic patching is performed
- Soft-reset and sleep patches are incompatible with some games
- No Nintendo DS Rumble Pak mode
- No Nintendo DS Browser RAM expansion
- No GBA-to-DS Link mode
- microSD cards larger than 32GB are not officially supported
- Discontinued and no longer receiving kernel updates

---

## Known Problems

### No Nintendo Logo

The console may not be making proper contact with the cartridge.

- Remove and reinsert the Reform
- Clean the cartridge contacts
- Test it in another console
- Check that the cartridge shell is assembled correctly

### Black Screen After the Nintendo Logo

The official Reform FAQ identifies this as a possible hardware failure.

If the problem continues with multiple consoles and microSD cards, the cartridge may require repair or replacement.

### White Screen or Crash After Loading to PSRAM

A white screen or crash immediately after a successful PSRAM write can indicate defective cartridge memory.

Test several verified clean ROMs and another microSD card. Persistent failures across multiple games usually indicate a hardware problem.

### Language Selection Appears Every Time

This normally indicates a weak, dead, incorrectly installed, or poorly connected CR1220 battery.

Replace the battery and confirm that its contacts are clean and making firm contact.

### Corrupted Menu Graphics or Text

Glitched menu graphics and text are commonly associated with a dead CR1220 battery.

Replace the battery before reinstalling the kernel or formatting the microSD card.

### `FAT initial 0`

The microSD card was not detected correctly.

- Remove and reinsert the microSD card
- Clean the microSD contacts
- Test another FAT32 microSD card

### `FAT initial 1`

The `ezfla_up.bin` file is incorrect, corrupted, or intended for another model.

Download a clean copy of EZ4 Kernel 2.05 from the official EZ-Flash website.

### Empty File Browser

If no files appear:

- Reinsert the microSD card
- Confirm that it is formatted as FAT32
- Test a smaller or different microSD card
- Move games closer to the root directory
- Avoid excessively deep folder structures

### Save Loss

Save loss can occur when:

- The CR1220 battery is dead
- The console is not restarted after saving
- The boot-time backup is skipped with `L`
- Another game is launched before the previous save is backed up
- The ROM and save filenames do not match
- The microSD card or filesystem is corrupted

### Freezing With Soft Reset or Sleep Enabled

Some games are incompatible with the GSS patch.

Launch the game with `L + B` to disable the soft-reset and sleep patch for that launch.

### ROM Hacks and Translations

Modified ROMs may use nonstandard save types, expanded ROM sizes, or altered anti-piracy routines that the automatic patcher does not recognize correctly.

Possible symptoms include:

- White screens
- Freezing
- Saves not being created
- Saves loading incorrectly
- Games working once but failing on later launches

Delete the corresponding file from the `PATCH` folder and allow the Reform to patch the ROM again. If the issue continues, test a verified clean base ROM or manually apply the correct save patch.

---

## Basic Troubleshooting

1. Install official EZ4Kernel 2.05.
2. Use a reputable microSD card no larger than 32GB.
3. Format the microSD card as FAT32.
4. Back up and then remove old files from the `PATCH` folder.
5. Test with a verified clean GBA ROM.
6. Launch the game with `L + B` to disable GSS.
7. Try a hard boot with `L + A`.
8. Replace the CR1220 battery if settings reset or graphics are corrupted.
9. Clean the cartridge and microSD contacts.
10. Test the Reform in another console.
11. Back up the `SAVER` folder before formatting or replacing the microSD card.

Persistent PSRAM failures, black screens after the Nintendo logo, or crashes across multiple consoles may indicate defective cartridge hardware.

---

## Notes

- Released in 2017
- Uses the same EZ4Kernel family as the EZ-Flash IV
- Latest official kernel is 2.05
- Uses the update file `ezfla_up.bin`
- Uses a replaceable CR1220 battery
- The battery retains SRAM and settings, not an RTC
- Includes interchangeable GBA and Nintendo DS Lite shells
- Replaced by the EZ-Flash Omega in 2018
- Keep regular backups of the `SAVER` folder
