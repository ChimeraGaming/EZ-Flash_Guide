# EZ-Flash III Software, OS, and Loader History

## Current Preserved Version

- PC software: EZ3Manager 2.22
- Update method: EZ3Manager with the EZ-Writer II
- Standalone kernel file: None
- Standalone firmware installer: None
- GBA operating system: Written to the cartridge through EZ3Manager
- Nintendo DS loader: `ndsloader.bin`
- Operating system requirement: Legacy 32-bit Windows

[Official EZ3Manager Download](https://www.ezflash.cn/download/)

[Official EZ3Manager Source Code](https://github.com/ez-flash/ez3manage)

EZ3Manager 2.22 is the final version currently distributed through the official EZ-FLASH legacy download page.

The EZ-Flash III does not use a removable-storage kernel file such as `ezfla_up.bin` or `ezkernel.bin`. Its software, operating system, loaders, patches, and cartridge data are managed through EZ3Manager and the EZ-Writer II.

---

## Terminology

The EZ-Flash III software is divided into several components.

### EZ3Manager

The Windows application used to:

- Detect the EZ-Writer II
- Detect the EZ-Flash III cartridge
- Format cartridge storage
- Write games to NAND and NOR
- Manage save files
- Apply game patches
- Install or repair the cartridge operating system
- Configure GBA and Nintendo DS functions
- Update XCODE compatibility data
- Install skins and system resources

### EZ3 OS

The menu and operating system stored in a dedicated area of the cartridge.

It provides:

- GBA game browsing
- NAND library management
- NAND-to-PSRAM loading
- NAND-to-NOR copying
- Save management
- Real-time save functions
- Cheat functions
- Settings
- Text and utility tools
- Skin support
- Cartridge maintenance functions

The EZ3 OS version is separate from the EZ3Manager version.

### `ndsloader.bin`

The Nintendo DS-mode loader used by compatible Nintendo DS configurations.

It is separate from the standard GBA menu and is included in later EZ3Manager packages.

### USB Driver

The Windows USB driver used to communicate with the EZ-Writer II.

The USB driver version is separate from:

- The EZ3Manager version
- The EZ3 OS version
- The Nintendo DS loader version

---

## Confirmed Version History

Only releases confirmed through an official download, preserved package, contemporary report, archived release discussion, or historical publication are included.

| EZ3Manager | Status | Confirmed Information |
| --- | --- | --- |
| 2.02 | Historical | Confirmed through contemporary EZ-Flash III support discussions. A complete changelog has not been preserved. |
| 2.03 | Historical | Added full backup of the cartridge's save directory to the computer and updated the XCODE and ROM-name databases. |
| 2.06 | Historical | Confirmed release from September 2005. A complete changelog has not been preserved. |
| 2.08 | Preserved GBA-focused release | Final confirmed release before Nintendo DS mode was introduced. Commonly recommended when only GBA functionality is required. |
| 2.09 Beta 1 | Historical beta | Early Nintendo DS compatibility release distributed through the official EZ-FLASH website. Included drivers for multiple EZ-Writer revisions. |
| 2.10 | Historical | Confirmed release distributed with EZ-Writer II and EZ-Flash III driver files. A complete changelog has not been preserved. |
| 2.20 | Historical late release | Included Nintendo DS functions, USB drivers, NAND and NOR management, and support for writing the Nintendo DS loader. |
| 2.21 | Historical late release | Documented with EZ3 OS 1.68 and USB Driver 1.54. |
| 2.22 | Final official preserved release | Final official release. Distributed with an updated `ndsloader.bin`. |

### Unconfirmed Version Numbers

Additional releases may have existed, but sufficiently reliable evidence has not been located for:

- Versions before 2.02
- Versions 2.04 and 2.05
- Version 2.07
- Versions 2.11 through 2.19

A missing version number does not prove that the release never existed.

Do not add undocumented versions or assign changes to a specific release unless an original package, release announcement, screenshot, or reliable contemporary reference is found.

---

## EZ3Manager 2.02

EZ3Manager 2.02 is the earliest currently confirmed release in this guide.

It is documented through contemporary EZ-Flash III troubleshooting and support discussions.

A complete release package or official changelog has not been preserved in a verifiable public archive.

Do not assign specific new features to EZ3Manager 2.02 without additional documentation.

---

## EZ3Manager 2.03

EZ3Manager 2.03 was released during the active development period of the EZ-Flash III.

### Documented Changes

- Added the ability to back up the entire cartridge save directory
- Stored the backup in the EZ3Manager installation's `Saver` directory
- Updated the XCODE compatibility database
- Updated the ROM-name database

The save-directory backup feature made it easier to preserve all cartridge saves before formatting, repairing, or reorganizing the EZ-Flash III.

The surviving changelog does not identify the exact XCODE or ROM-name database revisions included with the release.

---

## EZ3Manager 2.06

EZ3Manager 2.06 is a confirmed release from September 2005.

A complete official changelog has not been preserved.

The release belongs to the later GBA-focused development period before Nintendo DS mode became a standard part of EZ3Manager.

Specific compatibility fixes should not be attributed to 2.06 without an original release note or package documentation.

---

## EZ3Manager 2.08

EZ3Manager 2.08 is the final confirmed version before Nintendo DS mode was added.

It remains useful for owners who only need GBA functionality.

### Community-Reported Advantages

Compared with the later Nintendo DS-enabled releases, EZ3Manager 2.08 is commonly described as:

- Faster during some cartridge operations
- More reliable for GBA-only use
- Less complicated to configure
- Free from the later Nintendo DS loader functions

These are community observations rather than an official EZ-FLASH changelog.

Use EZ3Manager 2.08 when:

- Only GBA games are required
- Nintendo DS loading is not needed
- EZ3Manager 2.22 repeatedly freezes
- Later loader files cause problems
- A simpler GBA-focused installation is preferred

EZ3Manager 2.08 remains preserved through community archives.

---

## EZ3Manager 2.09 Beta 1

EZ3Manager 2.09 Beta 1 was distributed through the official EZ-FLASH website in late 2005 and early 2006.

It was an experimental release associated with early Nintendo DS compatibility.

### Confirmed Package Behavior

The package included drivers for multiple writer revisions, including files associated with:

- EZ-Writer
- EZ-Writer II
- EZ-Writer III
- EZ-Flash II
- EZ-Flash III

Some users had to remove the EZ-Writer II-specific driver files before Windows would correctly install the EZ-Flash III writer driver.

### Driver Warning

Do not randomly delete driver files from an archived package.

Different writer revisions require different files, and advice written for one specific setup may not apply to another.

Use a clean driver package and select the correct cartridge mode through `EZ_Mode.exe`.

Because 2.09 was a beta:

- Nintendo DS compatibility was incomplete
- Driver installation could be confusing
- Some games required additional patches
- Save support was incomplete for some Nintendo DS titles
- Loader behavior could vary between console revisions

EZ3Manager 2.08 is generally the safer choice for GBA-only use.

---

## EZ3Manager 2.10

EZ3Manager 2.10 is confirmed through contemporary use with EZ-Flash II and EZ-Flash III writer hardware.

The package contained multiple driver files, including:

`ezwinit2.sys`

This file was associated with EZ-Writer II operation.

A complete official changelog has not been preserved.

### Driver Compatibility

EZ3Manager packages sometimes supported more than one EZ-Flash product or writer revision.

Installing the wrong driver could cause:

- Writer not detected
- Cartridge not detected
- Repeated USB reconnection
- Incorrect cartridge capacity
- EZ3Manager remaining on initialization
- Writer indicator continuously flashing
- Windows repeatedly requesting another driver file

Use `EZ_Mode.exe` to select the correct device mode before starting EZ3Manager.

---

## EZ3Manager 2.20

EZ3Manager 2.20 is a confirmed late release from 2006.

It was widely distributed with the EZ-Writer USB drivers and included Nintendo DS-mode functionality.

### Confirmed Functions

- GBA game management
- Nintendo DS loader installation
- NAND library management
- 256Mbit NOR management
- Save management
- Cartridge formatting
- USB writer drivers
- EZ3 OS installation and repair
- PassMe and PassMe 2 configuration
- Loader replacement through the `SYSBIN` directory

### Memory Tabs

EZ3Manager 2.20 displays separate cartridge areas.

| Area | Purpose |
| --- | --- |
| 256 NOR | Persistent NOR storage, loaders, and directly executable games |
| NAND | Main long-term game and file library |

Nintendo DS configurations sometimes required writing a modified loader to the firmware area and storing the normal Nintendo DS loader in NOR.

These procedures were configuration-specific and should not be followed unless the required loader files and boot hardware are available.

---

## EZ3Manager 2.21

EZ3Manager 2.21 is documented with the following component versions:

- EZ3Manager: 2.21
- EZ3 OS: 1.68
- USB Driver: 1.54

These are separate version numbers.

Do not combine them into a single version such as `2.21.1.68`.

A complete EZ3Manager 2.21 changelog has not been preserved.

The version is useful as evidence that EZ3Manager, the cartridge OS, and the USB driver were updated independently.

---

## EZ3Manager 2.22

EZ3Manager 2.22 is the final official version currently available from EZ-FLASH.

### Confirmed Release Information

The original release archive contained:

- EZ3Manager 2.22
- An updated `ndsloader.bin`

The developer noted that a more complete manager update would be prepared later, but no later official version is currently preserved.

### Included Components

The surviving EZ3Manager source and package structure include:

- GBA and Nintendo DS loading resources
- USB communication code
- NAND and NOR management
- Save reading and writing tools
- Cheat data
- XCODE patching data
- Skin resources
- Language resources
- EZ3 OS installation files
- Nintendo DS loader files
- Cartridge erase, verify, and recovery functions

### Recommended Use

Use EZ3Manager 2.22 when:

- Nintendo DS loader support is required
- The latest preserved compatibility resources are wanted
- A cartridge requires the final official manager
- Earlier versions cannot identify the cartridge correctly

Use EZ3Manager 2.08 when:

- Only GBA games are needed
- The later Nintendo DS functionality is unnecessary
- 2.22 repeatedly freezes or performs poorly

---

## Version Relationships

EZ3Manager releases can contain several independently versioned components.

| Component | Example Version | Purpose |
| --- | --- | --- |
| EZ3Manager | 2.21 | Windows cartridge-management application |
| EZ3 OS | 1.68 | GBA menu and operating system stored on the cartridge |
| USB Driver | 1.54 | Windows communication driver for the EZ-Writer II |
| `ndsloader.bin` | Not normally shown | Nintendo DS-mode loader |
| XCODE | Date or game-number revision | Game patching and compatibility database |
| ROM-name list | Date or game-number revision | Game identification database |

Installing a newer EZ3Manager does not guarantee that every included component received a new version.

A release may update only:

- The Windows manager
- EZ3 OS
- USB driver
- `ndsloader.bin`
- XCODE data
- ROM-name data
- Cheat files
- Language files
- Skins
- Individual game patches

---

## Installation and Setup

1. Back up all accessible saves and cartridge data.
2. Use Windows XP 32-bit or a compatible legacy Windows environment.
3. Extract the complete EZ3Manager package.
4. Do not separate the executable from its folders.
5. Run `EZ_Mode.exe`.
6. Select `EZ3`.
7. Close the mode-selection utility.
8. Connect the EZ-Writer II directly to a powered USB port.
9. Avoid unpowered USB hubs.
10. Install the USB driver from the selected EZ3Manager package.
11. Insert the EZ-Flash III cartridge into the writer.
12. Start EZ3Manager.
13. Wait for the writer and cartridge to be detected.
14. Confirm that the displayed cartridge capacity is correct.
15. Do not format or write the cartridge if the capacity is incorrect.
16. Allow initialization to finish before selecting another function.

The EZ-Writer II may disconnect and reconnect during initialization.

Windows or virtualization software may treat the reconnected writer as a new USB device.

---

## Updating or Repairing the EZ3 OS

The EZ3 OS is installed through EZ3Manager.

There is no removable-storage update file equivalent to:

- `ezfla_up.bin`
- `ezkernel.bin`
- `ezkernelnew.bin`
- `ezbluekernel.bin`
- `ezairkernel.bin`

### OS Installation Procedure

1. Export all accessible saves.
2. Back up important NAND files.
3. Connect the cartridge through the EZ-Writer II.
4. Run `EZ_Mode.exe`.
5. Select `EZ3`.
6. Start EZ3Manager.
7. Confirm that the cartridge and its correct capacity are detected.
8. Open the appropriate system or operating-system function.
9. Install or repair the EZ3 OS.
10. Do not disconnect the writer during the operation.
11. Restart the cartridge and confirm that the GBA menu loads.
12. Restore games and saves only after the menu is working.

Formatting or reinstalling the OS can erase cartridge data.

Do not use OS reinstallation as the first troubleshooting step unless backups have already been created.

---

## GBA XCODE Compatibility Updates

GBA compatibility definitions were sometimes distributed separately from EZ3Manager.

A preserved update identified as:

```text
GBA XCODE 2805
2008-08-28
```

was intended for:

- EZ-Flash I
- EZ-Flash II
- EZ-Flash III
- EZ-Flash IV
- EZ-Flash V with 3-in-1

### Installing XCODE Data

1. Close EZ3Manager.
2. Back up the current `sysbin` folder.
3. Extract the XCODE package.
4. Copy the updated files into the EZ3Manager `sysbin` folder.
5. Replace the older files with the same names.
6. Restart EZ3Manager.
7. Rewrite affected games when required.

XCODE contains game-patching and compatibility information.

It is not:

- A new EZ3Manager release
- A new EZ3 OS
- Cartridge firmware
- A USB driver
- A Nintendo DS loader

Translated games, ROM hacks, and modified ROMs may not match the official XCODE database.

---

## Cartridge Memory Areas

EZ3Manager controls several types of memory inside the EZ-Flash III.

| Memory Area | Typical Purpose |
| --- | --- |
| NAND | Long-term game and file library |
| PSRAM | Temporary fast-loading memory |
| 256Mbit NOR | Persistent directly executable game storage |
| Firmware NOR | Stores the EZ3 OS or selected loader |
| SRAM | Active game-save storage |
| Real-time save area | Stores instant-save data |

The exact NAND capacity depends on the cartridge model.

Common EZ-Flash III capacities were marketed as:

- 1G
- 2G
- 4G
- 8G

These capacities are measured in gigabits rather than gigabytes.

---

## Game Management

EZ3Manager displays separate areas for the NAND library and NOR storage.

### NAND Library

- Stores the main game library
- Can contain many GBA games
- Files are added and removed through EZ3Manager
- Selected games are transferred to PSRAM or NOR before execution
- Transfer speed is slow compared with modern flashcarts
- File names may be shortened by the cartridge menu

### PSRAM

- Used for temporary game loading
- Loses its contents when power is removed
- Faster to rewrite than NOR
- Intended for games that fit within the supported PSRAM capacity

### NOR

- Stores frequently played games
- Retains data without power
- Supports direct execution
- Required for some large GBA games
- Can contain loaders and other persistent files
- Takes longer to write than PSRAM

Do not interrupt a NAND-to-NOR operation.

Large games may take several minutes to transfer.

---

## Save Management

The EZ-Flash III uses cartridge SRAM and NAND storage for save handling.

Depending on the selected mode:

- Active save data is held in SRAM
- EZ3 OS backs the save up to NAND
- EZ3Manager can import and export save files
- Real-time save data is stored separately
- Save-type patches may be applied when a game is written

### Before Formatting or Repairing

1. Open EZ3Manager.
2. Export every accessible normal save.
3. Export important real-time save data.
4. Use the full save-directory backup when available.
5. Confirm that the files were created on the computer.
6. Keep a second copy outside the EZ3Manager installation directory.
7. Confirm which game belongs to each save.

A weak or failed cartridge battery may affect save retention.

Do not format the cartridge until save backups have been verified.

---

## Nintendo DS Loader

Later EZ3Manager releases support:

`ndsloader.bin`

This file provides Nintendo DS-mode loading.

Nintendo DS operation may also require:

- Original Nintendo DS or Nintendo DS Lite
- PassMe
- PassMe 2
- EZ-Pass
- FlashMe
- A compatible loader configuration
- Correct Nintendo DS patches
- A supported game
- A compatible save type

### PassMe and PassMe 2

Earlier silver Nintendo DS systems could use the original PassMe design.

Later Nintendo DS firmware revisions generally required:

- PassMe 2
- Another compatible boot device
- FlashMe
- A later no-pass device

EZ3Manager includes options associated with:

- Writing the EZ3 Nintendo DS loader
- PassMe compatibility
- PassMe 2 compatibility
- Nintendo DS ROM patching
- Nintendo DS save handling

Nintendo DS support should be considered secondary and experimental compared with the cartridge's GBA functions.

---

## Nintendo DS Compatibility Limits

Nintendo DS compatibility can be affected by:

- Console firmware revision
- PassMe or PassMe 2 type
- FlashMe version
- `ndsloader.bin` revision
- EZ3Manager version
- Game size
- Save type
- Anti-piracy protection
- Download Play
- Nintendo Wi-Fi functions
- Sleep mode
- Later Nintendo DS hardware
- Modified or translated ROMs

A Nintendo DS game failing to load does not automatically indicate defective EZ-Flash III hardware.

Test normal GBA operation separately.

EZ3Manager 2.08 does not include the later Nintendo DS-mode functions.

---

## Themes and Skins

The EZ3 GBA operating system supports skins.

Skin resources are stored and managed through EZ3Manager and its included directories.

The official source tree contains several `.ssk` skin files.

Before installing a custom skin:

- Confirm that it was designed for EZ-Flash III
- Confirm which EZ3 OS version it supports
- Back up the original system files
- Back up all saves
- Keep a clean EZ3Manager package
- Test the official OS before diagnosing menu problems

An incompatible skin can cause:

- Missing menu graphics
- Corrupted text
- Incorrect language files
- Freezing
- Blank screens
- Failed OS installation
- Missing cartridge functions

---

## Modern Windows Compatibility

EZ3Manager and the EZ-Writer II driver were designed for legacy Windows.

The most reliable environments are:

- Windows XP 32-bit
- A physical legacy Windows computer
- A Windows XP 32-bit virtual machine with USB passthrough

Modern 64-bit Windows may reject the unsigned USB driver.

### Virtual Machine Setup

1. Create a Windows XP 32-bit virtual machine.
2. Enable USB passthrough.
3. Install EZ3Manager inside the virtual machine.
4. Run `EZ_Mode.exe` and select `EZ3`.
5. Connect the EZ-Writer II to the host computer.
6. Attach the writer to the Windows XP guest.
7. Install the matching USB driver.
8. Watch for the writer to disconnect and reconnect.
9. Attach the reconnected device to the guest again when required.
10. Start EZ3Manager only after the writer appears inside Windows XP.

Avoid the original online update function.

Its remote services are no longer reliable.

Use locally preserved manager, driver, loader, and XCODE files.

---

## Known Problems

### Writer Not Detected

Possible causes include:

- Missing USB driver
- Wrong driver for the writer revision
- Incorrect selection in `EZ_Mode.exe`
- Unsupported 64-bit Windows environment
- USB passthrough not enabled
- Writer connected through a USB hub
- Writer reconnecting under another USB identifier
- Damaged USB cable
- Failed EZ-Writer II hardware

Connect the writer directly and test it under Windows XP 32-bit.

---

### Cartridge Not Detected

- Clean the cartridge contacts
- Reinsert the cartridge firmly
- Restart EZ3Manager
- Reconnect the writer
- Run `EZ_Mode.exe`
- Confirm that `EZ3` is selected
- Test another direct USB port
- Reinstall the matching driver
- Test another confirmed EZ3Manager release

---

### Cartridge Repeatedly Requests Formatting

Do not immediately approve formatting.

A repeated format request can be caused by:

- Incorrect mode selected in `EZ_Mode.exe`
- Incompatible EZ3Manager version
- USB driver communication failure
- Corrupted NAND filesystem
- Damaged EZ3 OS
- Failing NAND memory
- Poor cartridge contact
- Incorrect cartridge-capacity detection

Attempt to export saves before formatting.

---

### Incorrect Cartridge Capacity

Do not write or format the cartridge when EZ3Manager reports the wrong capacity.

Possible causes include:

- Incorrect writer driver
- Failed USB communication
- Incorrect mode selection
- Poor cartridge contact
- Unsupported writer revision
- Failing NAND memory
- Damaged cartridge hardware

Reconnect the writer and correct the detection problem before continuing.

---

### EZ3Manager Freezing

EZ3Manager can appear frozen during:

- Large NAND transfers
- Formatting
- File deletion
- NAND-to-NOR copying
- Driver reconnection
- Corrupted-file handling
- Nintendo DS patching
- Cartridge verification

Wait for USB and storage activity to stop before ending the process.

Interrupting the program during a write can corrupt cartridge data.

EZ3Manager 2.08 may be preferable when only GBA functions are needed.

---

### Eight-Character Filenames

The EZ-Flash III menu may shorten game names to an eight-character format.

Large libraries can contain several similarly named entries.

Use short, unique names before transferring games.

---

### Corrupted NAND Files

A failed transfer can leave a damaged game entry in NAND.

1. Attempt to delete the affected entry through EZ3Manager.
2. Restart the manager.
3. Transfer the file again.
4. Test another source ROM.
5. Back up saves before formatting NAND.

Do not format the full cartridge unless other recovery methods fail.

---

### Nintendo DS Loader Problems

Possible symptoms include:

- White screen
- Black screen
- Loader menu not appearing
- Corrupted game names
- Save failure
- Game loading only after opening the NOR area first
- Game requiring PassMe 2 mode
- Game working with one loader and failing with another

Confirm:

- Correct `ndsloader.bin`
- Correct boot hardware
- Correct console firmware support
- Correct EZ3Manager version
- Correct save patch
- Correct loader installation

Do not replace `ndsloader.bin` with a loader intended for another EZ-Flash product.

---

### Save Loss

Possible causes include:

- Failed cartridge battery
- Save not copied from SRAM
- Cartridge formatted before saves were exported
- Incorrect save type
- Damaged NAND filesystem
- Wrong save restored
- Real-time save conflict
- Interrupted write
- Game patched with incorrect XCODE data

Keep external backups of every important save.

---

### USB Reconnection

The writer may disconnect and reconnect during initialization or cartridge operations.

In a virtual machine, the reconnected writer may appear as a new USB device.

Attach it to the Windows XP guest again before restarting EZ3Manager.

---

## Recovery Utilities

Some archived EZ-Flash III packages include:

`EZ3Check.exe`

This utility can erase or repair cartridge data when EZ3Manager repeatedly requests formatting or cannot initialize the cartridge.

Using EZ3Check can erase the cartridge completely.

Before using it:

1. Export all accessible saves.
2. Confirm that EZ3Manager cannot repair the problem normally.
3. Confirm that the correct cartridge is connected.
4. Use a stable USB connection.
5. Do not interrupt the erase or repair operation.
6. Reinstall the EZ3 OS after the utility finishes.

Use EZ3Check only as a recovery tool.

---

## Upgrade and Usage Warnings

- EZ3Manager 2.22 is the final official preserved release.
- EZ3Manager 2.08 is the final confirmed GBA-focused release before DS mode.
- There is no standalone kernel update file.
- Back up saves before formatting or reinstalling the EZ3 OS.
- Do not interrupt NAND, NOR, OS, save, or loader operations.
- Confirm that EZ3Manager detects the correct cartridge capacity.
- Use `EZ_Mode.exe` to select the correct hardware.
- Connect the EZ-Writer II directly to the computer.
- Avoid the original online updater.
- Do not install EZ-Flash IV or Omega-family kernels.
- Do not mix `ndsloader.bin` files from unrelated products.
- Do not mix random USB drivers from different packages.
- Keep archived copies of the complete manager, driver, `sysbin`, skins, and loader files.
- Scan third-party archives before running preserved executables.

---

## Notes

- EZ3Manager 2.02 is the earliest currently confirmed release.
- EZ3Manager 2.03 added full save-directory backup.
- EZ3Manager 2.06 is a confirmed September 2005 release.
- EZ3Manager 2.08 is the final confirmed GBA-focused version.
- EZ3Manager 2.09 Beta 1 introduced experimental Nintendo DS-era functions.
- EZ3Manager 2.10 is a confirmed driver and manager release.
- EZ3Manager 2.20 is a confirmed late Nintendo DS-enabled release.
- EZ3Manager 2.21 is documented with EZ3 OS 1.68 and Driver 1.54.
- EZ3Manager 2.22 is the final official version.
- EZ3Manager is the PC client, not the cartridge kernel.
- The EZ3 OS is stored in dedicated cartridge memory.
- `ndsloader.bin` is separate from the GBA operating system.
- GBA support is more complete than Nintendo DS support.
- Legacy Windows and the original EZ-Writer II are normally required.
- Keep external backups of saves and working software.

---

## Sources

- [Official EZ-FLASH Download Page](https://www.ezflash.cn/download/)
- [Official EZ3Manager Source Code](https://github.com/ez-flash/ez3manage)
- [EZ3Manager 2.22 Release Discussion](https://gbatemp.net/threads/ez3-manager-2-22.38498/)
- [EZ3Manager 2.08 Archive](https://gbatemp.net/download/ez3manager-2-08.38265/)
- [EZ3Manager 2.09 Beta Discussion](https://www.elotrolado.net/hilo_software-ez3_497259)
- [EZ3Manager 2.10 Driver Discussion](https://www.elotrolado.net/hilo_carga-de-flashme-gba_654701)
- [EZ3Manager 2.20 Setup Tutorial](https://www.elotrolado.net/hilo_tutorial-como-cargar-homebrew-y-backups-con-el-max-media-launcher-y-ezflash-iii_565608)
- [EZ3Manager 2.21 Component Versions](https://gbatemp.net/threads/ez-flash-3-my-first-24-hours.77208/)
- [EZ-Flash III Wiki](https://wiki.gbatemp.net/wiki/EZ-Flash_III)
- [EZ-Flash III Review](https://dsdatabase.org/ezflashiii.html)
- [EZ-Flash Cartridge History](https://gbasp.ru/ezflashhistory1-en.html)
- [Preserved GBA XCODE Information](https://bbs.newwise.com/thread-232523-1-1.html)
