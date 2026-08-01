# EZ-Flash III Software, OS, and Loader History

## Current Preserved Version

- PC software: EZ3Manager 2.22
- Update method: Through EZ3Manager and the EZ-Writer II
- Separate kernel file: None
- Separate firmware installer: None
- GBA operating system: Written to the cartridge by EZ3Manager
- Nintendo DS loader: `ndsloader.bin`
- Operating system: Legacy 32-bit Windows

[Official EZ3Manager Download](https://www.ezflash.cn/download/)

EZ3Manager 2.22 is the final version currently provided through the official EZ-FLASH legacy download page.

---

## Terminology

The EZ-Flash III software is divided into several components.

### EZ3Manager

The Windows application used to:

- Detect the EZ-Writer II
- Format cartridge storage
- Write games to NAND and NOR
- Manage save files
- Apply game patches
- Install or repair the cartridge operating system
- Configure GBA and Nintendo DS features

### EZ3 OS

The menu and operating system stored in the cartridge's dedicated firmware area.

It provides:

- GBA game browsing
- NAND-to-PSRAM loading
- NAND-to-NOR copying
- Save management
- Settings
- Text tools
- Skins
- Cartridge utilities

### `ndsloader.bin`

The Nintendo DS-mode loader used by compatible Nintendo DS setups.

It is separate from the normal GBA menu and is included in the EZ3Manager software package.

### Driver

The Windows USB driver used to communicate with the EZ-Writer II.

The driver version displayed by EZ3Manager is not the same as the cartridge OS version.

---

## Version History

| EZ3Manager | Known Components or Changes |
| --- | --- |
| 2.22 | Final official preserved release. Distributed with an updated `ndsloader.bin`. |
| 2.21 | Documented with EZ3 OS 1.68 and Driver 1.54. |
| 2.20 | Widely distributed late release. A complete official changelog is not preserved. |
| 2.09 Beta 1 | Experimental Nintendo DS compatibility release. Compatibility was incomplete. |
| 2.08 | Preserved GBA-focused package without the later Nintendo DS functions. |
| 2.03 | Early 2005 release from the active EZ-Flash III development period. |
| Earlier versions | Historical releases existed, but a complete official version history is not currently preserved. |

Do not assume that every EZ3Manager release included a new EZ3 OS or USB driver.

Some releases changed only:

- The PC manager
- Game patches
- Nintendo DS loader files
- Compatibility databases
- Included system resources

---

## EZ3Manager 2.22

EZ3Manager 2.22 is the final official version currently available from EZ-FLASH.

The preserved release package included:

- Updated `EZManager.exe`
- A newer `ndsloader.bin`
- EZ-Flash III system files
- USB driver files
- Game-patching resources
- Files contained in the `sysbin` directory

A full official changelog for every file in the package is not currently available.

Do not claim that EZ3Manager 2.22 updates the GBA OS beyond version 1.68 unless the installed cartridge reports a different version.

---

## EZ3Manager 2.21

A documented EZ3Manager 2.21 installation reported:

- EZ3 OS Version: 1.68
- Driver Version: 1.54

These numbers identify separate components.

- `2.21` is the PC manager version.
- `1.68` is the cartridge's GBA operating-system version.
- `1.54` is the EZ-Writer driver version reported by the manager.

The version numbers should not be combined into a single kernel number.

---

## Installation and Setup

1. Back up all accessible saves and cartridge data.
2. Use a legacy 32-bit Windows installation or Windows XP virtual machine.
3. Install the EZ-Writer II USB driver.
4. Connect the EZ-Writer II directly to a powered USB port.
5. Avoid unpowered USB hubs.
6. Insert the EZ-Flash III cartridge into the writer.
7. Run `EZ_Mode.exe` and select `EZ3` when the package includes the mode-selection utility.
8. Start EZ3Manager 2.22.
9. Wait for the writer and cartridge to be detected.
10. Confirm that the reported cartridge capacity is correct.
11. Allow EZ3Manager to initialize the cartridge.
12. Update or reinstall the EZ3 OS only when required.
13. Do not disconnect the writer during any write, format, or repair operation.

The EZ-Writer II may not initialize correctly through a USB hub.

---

## Updating the EZ3 OS

The EZ3 OS is installed through EZ3Manager.

There is no removable storage card and no file equivalent to:

- `ezfla_up.bin`
- `ezkernel.bin`
- `ezkernelnew.bin`
- `ezbluekernel.bin`
- `ezairkernel.bin`

To reinstall or repair the operating system:

1. Back up saves and important NAND files.
2. Connect the cartridge through the EZ-Writer II.
3. Start EZ3Manager 2.22.
4. Confirm that the cartridge is detected correctly.
5. Use the manager's operating-system or formatting function.
6. Allow the full operation to complete.
7. Reconnect the cartridge if requested.
8. Confirm that the GBA menu starts before restoring additional files.

Formatting the cartridge can erase its NAND contents.

Do not reinstall the OS as a first troubleshooting step unless backups already exist.

---

## GBA XCODE Compatibility Updates

Later GBA compatibility definitions were distributed separately from the main manager.

A preserved GBA XCODE update identified as `2805`, dated August 28, 2008, supported:

- EZ-Flash I
- EZ-Flash II
- EZ-Flash III
- EZ-Flash IV
- EZ-Flash V with 3-in-1

For EZ3Manager:

1. Close EZ3Manager.
2. Back up the current `sysbin` folder.
3. Extract the updated XCODE package.
4. Copy the files into `sysbin`.
5. Replace the older files with the same names.
6. Restart EZ3Manager.

XCODE is game-patching data and is not a new EZ3 OS.

Translated games and modified ROMs may not match the official patch database.

---

## GBA Storage Areas

EZ3Manager controls several different memory areas inside the cartridge.

| Area | Typical Purpose |
| --- | --- |
| NAND | Long-term library storage |
| PSRAM | Temporary fast loading for games up to its supported size |
| 256Mbit NOR | Persistent storage and direct execution |
| Firmware NOR | Stores the EZ3 operating system |
| SRAM | Active save storage |

The exact NAND capacity depends on the EZ-Flash III model.

Common models were marketed as:

- 1G
- 2G
- 4G
- 8G

These capacities were advertised in gigabits.

---

## Game Management

EZ3Manager presents separate areas for the cartridge's NAND library and NOR memory.

### NAND Library

- Stores the main game library
- Files can be added or removed through EZ3Manager
- Games are copied to PSRAM or NOR before execution
- Transfer speed is slow by modern standards
- File names may be restricted to short formats

### NOR Area

- Stores frequently played games
- Supports direct execution
- Required for 256Mbit / 32MB GBA games
- Can hold several smaller games when capacity permits
- Can be managed from the cartridge menu

Do not interrupt a NAND-to-NOR copy.

Large games can take several minutes to copy.

---

## Save Management

EZ-Flash III saves involve both cartridge SRAM and NAND storage.

Depending on the selected mode and game:

- The active save is held in SRAM
- The cartridge OS backs the save up to NAND
- EZ3Manager can import or export save files
- Real-time save data is stored separately from normal game saves

Before formatting or repairing the cartridge:

1. Export all accessible saves through EZ3Manager.
2. Back up any visible save files.
3. Confirm the backups can be read from the computer.
4. Keep a second copy outside the EZ3Manager directory.

A failed or weak cartridge battery may affect save retention.

---

## Nintendo DS Loader

EZ3Manager 2.22 included an updated:

`ndsloader.bin`

This file is used for Nintendo DS-mode loading.

Nintendo DS operation may also require:

- An original Nintendo DS or DS Lite
- FlashMe
- A compatible PassMe or EZ-Pass device
- Correct DS-mode patches
- A compatible game
- Correctly installed loader files

Nintendo DS support is secondary to the cartridge's GBA functions.

Compatibility is incomplete, especially with:

- Later Nintendo DS games
- Download Play
- Nintendo Wi-Fi features
- Nintendo DS homebrew
- Games requiring newer save types
- Games using unsupported anti-piracy systems

Do not replace `ndsloader.bin` with a file from another EZ-Flash model.

---

## Themes and Skins

The EZ3 GBA operating system supports skins.

Skin files and system resources are managed through EZ3Manager and its included folders.

Before installing a custom skin:

- Confirm that it is designed for the EZ-Flash III
- Back up the original system files
- Confirm which EZ3 OS version it supports
- Keep a clean copy of EZ3Manager 2.22
- Test the official OS before troubleshooting menu problems

An incompatible skin can cause:

- Missing menu graphics
- Corrupted text
- Freezing
- Blank screens
- Incorrect language files
- Failed operating-system installation

---

## Modern Windows Compatibility

EZ3Manager and the EZ-Writer II driver were designed for legacy Windows.

The most reliable environment is:

- Windows XP 32-bit
- A physical older computer
- A Windows XP virtual machine with USB passthrough

Modern 64-bit Windows may reject the unsigned USB driver.

When using a virtual machine:

1. Pass the EZ-Writer II through to the guest.
2. Install the driver inside Windows XP.
3. Watch for the writer to reconnect during initialization.
4. Pass it through again when it appears as another USB device.
5. Restart EZ3Manager only after the writer is visible inside the guest.

Avoid the built-in online update function. Its original update service is no longer reliable.

Use a complete locally archived EZ3Manager 2.22 package instead.

---

## Known Problems

### Writer Not Detected

Possible causes include:

- Missing driver
- Unsupported 64-bit Windows environment
- USB hub incompatibility
- Virtual-machine passthrough not enabled
- Writer reconnecting under another USB identifier
- Damaged USB cable
- Failed EZ-Writer II hardware

Connect the writer directly and test it under Windows XP.

### Cartridge Requests Formatting

Do not immediately approve formatting.

A repeated format request can be caused by:

- Incorrect mode selected in `EZ_Mode.exe`
- Incompatible EZManager version
- Driver communication failure
- Damaged NAND filesystem
- Corrupted EZ3 OS
- Failing NAND memory
- Poor cartridge contact

Attempt to export saves before formatting.

### Incorrect Capacity

Do not write or format the cartridge if EZ3Manager reports the wrong capacity.

Reconnect the writer, restart Windows, reinstall the driver, and test another USB port.

### Manager Freezing

EZ3Manager can freeze during:

- Large NAND transfers
- Formatting
- File deletion
- Driver reconnection
- Corrupted-file handling
- Incompatible Nintendo DS patching

Wait for disk and USB activity to stop before ending the process.

Interrupting the program during a write can corrupt cartridge data.

### Eight-Character Filenames

The EZ-Flash III menu may reduce names to an eight-character format.

Large libraries can therefore contain several similarly named files.

Use short, unique names before transferring games.

### Corrupted Files

A failed transfer can leave a corrupted game entry in NAND.

Delete the affected entry through EZ3Manager and transfer it again.

If deletion fails, back up the cartridge and consider reformatting the affected area.

### Nintendo DS Compatibility

The later EZ3Manager releases added experimental Nintendo DS support, but many games remain incompatible.

Nintendo DS failure does not necessarily indicate defective cartridge hardware.

Test normal GBA operation separately.

### Save Loss

Possible causes include:

- Failed battery
- Save not backed up from SRAM
- Cartridge formatted before saves were exported
- Incorrect save type
- Damaged NAND filesystem
- Wrong game's save restored
- Real-time save conflict
- Interrupted write

Keep external backups of every important save.

---

## Upgrade Warnings

- EZ3Manager 2.22 is the final official preserved release.
- There is no standalone kernel update file.
- Back up saves before formatting or reinstalling the EZ3 OS.
- Do not interrupt NAND, NOR, OS, or save operations.
- Confirm that EZ3Manager detects the correct cartridge capacity.
- Connect the EZ-Writer II directly to the computer.
- Avoid the original online updater.
- Do not install EZ-Flash IV or Omega-family kernels.
- Do not mix `ndsloader.bin` files from unrelated products.
- Keep archived copies of the complete manager, driver, `sysbin`, and loader files.
- Scan third-party archives before running preserved executables.

---

## Notes

- EZ3Manager 2.22 is the final official version.
- EZ3Manager is the PC client, not the cartridge kernel.
- The EZ3 OS is written to dedicated cartridge memory.
- EZ3Manager 2.21 is documented with EZ3 OS 1.68 and Driver 1.54.
- EZ3Manager 2.22 included an updated `ndsloader.bin`.
- The manager controls NAND, PSRAM, NOR, SRAM, and firmware storage.
- GBA support is substantially better than its experimental Nintendo DS support.
- Legacy Windows and the original EZ-Writer II are normally required.
- Keep external backups of saves and working software.

---

## Sources

- [Official EZ-FLASH Download Page](https://www.ezflash.cn/download/)
- [EZ3Manager 2.22 Release Discussion](https://gbatemp.net/threads/ez3-manager-2-22.38498/)
- [EZ-Flash III Wiki](https://wiki.gbatemp.net/wiki/EZ-Flash_III)
- [EZ-Flash III Review](https://dsdatabase.org/ezflashiii.html)
- [EZ-Flash Cartridge History](https://gbasp.ru/ezflashhistory1-en.html)
