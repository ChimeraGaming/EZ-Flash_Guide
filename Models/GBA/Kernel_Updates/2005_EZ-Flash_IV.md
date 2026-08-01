# EZ-Flash IV Kernel History

## Current Version

- Kernel: 2.05
- Update file: `ezfla_up.bin`
- SHA-1: `2884e3e622f100250660bc2810245ba552b90cdb`
- Separately numbered firmware: None
- Shared kernel family:
  - EZ-Flash IV MicroSD
  - EZ-Flash Reform

[Official Kernel Download](https://www.ezflash.cn/download/)

[Official EZ-Flash IV Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)

The official download page currently lists Kernel 2.05 under `EZ-FLASH IV MicroSD`.

Kernel 2.04 added support for the EZ-Flash Reform, allowing both models to use the same EZ4Kernel family.

---

## Update Instructions

1. Start the EZ-Flash IV normally.
2. Allow any pending save backup to finish.
3. Do not press `L` during startup because that skips the save backup.
4. Back up the `SAVE` folder from the storage card.
5. Download and extract the official Kernel 2.05 package.
6. Place `ezfla_up.bin` in the root of the storage card.
7. Insert the card into the EZ-Flash IV.
8. Hold `R` while powering on the console.
9. Keep the console powered until the installation finishes.
10. Confirm that version `2.05` appears in the upper-right corner of the menu.
11. Delete `ezfla_up.bin` after the update completes.

Do not turn off the console during the update.

---

## Version History

| Kernel | Changes |
| --- | --- |
| 2.05 | Latest official release. EZ-FLASH currently provides the download and SHA-1 hash but does not publish a separate detailed changelog. |
| 2.04 | Added support for the EZ-Flash Reform. EZ-Flash IV users were told they could either update or remain on Kernel 2.03. |
| 2.03 | Added a global GSS switch and individual per-game GSS controls through `KEYSET.CFG`. |
| 2.02 | Introduced Global Soft Reset and Sleep, customizable hotkeys, and the option to launch incompatible games without the GSS patch. |
| 2.01 | Improved the Auto Patch Engine by saving generated patch data after the first launch and reusing it during later launches. |
| 2.00 | Introduced the onboard Auto Patch Engine, allowing clean ROMs to be copied directly to the storage card without processing them on a computer first. |
| 1.78 | Removed the previous limit of 78 files in the root directory. Subfolders remained limited to 99 files for performance reasons. |

A complete official changelog for kernels older than 1.78 is not currently preserved on the EZ-FLASH website.

---

## Kernel 2.05

Kernel 2.05 is the latest official EZ4Kernel release currently available from EZ-FLASH.

### Officially Published Information

- Update file: `ezfla_up.bin`
- SHA-1: `2884e3e622f100250660bc2810245ba552b90cdb`
- Listed for the EZ-Flash IV MicroSD
- Retains the EZ-Flash Reform support introduced in Kernel 2.04

EZ-FLASH has not published a separate detailed changelog identifying what changed between Kernel 2.04 and Kernel 2.05.

Do not assign specific compatibility fixes to Kernel 2.05 unless an official changelog or package documentation is found.

---

## Kernel 2.04

Kernel 2.04 added support for the EZ-Flash Reform.

### Changes

- Added EZ-Flash Reform hardware support
- Continued support for compatible EZ-Flash IV hardware
- Retained the Auto Patch Engine
- Retained Global Soft Reset and Sleep
- Retained configurable GSS controls

The official announcement stated that EZ-Flash IV owners could update to Kernel 2.04 or remain on Kernel 2.03.

Kernel 2.04 did not announce a new EZ-Flash IV-specific feature.

---

## Kernel 2.03

Kernel 2.03 expanded the GSS configuration introduced in Kernel 2.02.

### Changes

- Added a global GSS enable or disable switch
- Added individual per-game GSS controls
- Added the new settings to `KEYSET.CFG`

This allows GSS to remain enabled for most games while being disabled for specific incompatible games.

---

## Kernel 2.02

Kernel 2.02 introduced Global Soft Reset and Sleep, abbreviated as GSS.

### Changes

- Added return-to-menu soft reset
- Added sleep mode
- Added configurable hotkeys
- Added `KEYSET.CFG`
- Added the ability to launch a game without the GSS patch

### Default Hotkeys

| Function | Default Hotkey |
| --- | --- |
| Return to the EZ-Flash menu | `L + Up + B` |
| Enter sleep mode | `L + R + Start` |
| Wake from sleep | `Start + Select` |

The `KEYSET.CFG` file must be placed in the root of the storage card.

### Game-Loading Controls

| Control | Function |
| --- | --- |
| `A` | Launch normally |
| `L + A` | Launch using hard reset |
| `L + B` | Launch without GSS |
| `SELECT` | Write game to NOR |
| `L + SELECT` | Write game to NOR without GSS |

Some games cannot be patched correctly with GSS.

Use `L + B` when a game freezes, displays a blank screen, or otherwise fails with soft reset and sleep enabled.

---

## Kernel 2.01

Kernel 2.01 improved the Auto Patch Engine introduced in Kernel 2.00.

### Changes

- Generated reusable patch data after a game's first launch
- Stored generated patches in the `PATCH` folder
- Skipped the full patching process during later launches
- Reduced repeat-launch loading times

### Published Loading-Time Comparison

| ROM Size | First Launch | Later Launch | Kernel 1.78 |
| --- | ---: | ---: | ---: |
| 32Mbit | 27 seconds | 9 seconds | 16 seconds |
| 64Mbit | 51 seconds | 18 seconds | 25 seconds |
| 128Mbit | 100 seconds | 33 seconds | 52 seconds |

The first launch remained similar to Kernel 2.00 because the ROM still had to be analyzed and patched.

Later launches became faster because the generated patch file was reused.

---

## Kernel 2.00

Kernel 2.00 introduced the onboard Auto Patch Engine, abbreviated as APE.

### Changes

- Added automatic ROM patching on the cartridge
- Added automatic save-type patching
- Allowed clean GBA ROMs to be copied directly to the storage card
- Removed the normal requirement to process each ROM on a computer
- Created the foundation for the reusable patch system added in Kernel 2.01

Generated patch files are stored in:

```text
/PATCH/
```

A new patch should be generated when:

- A ROM is replaced with another revision
- A translation is updated
- A ROM hack is updated
- The ROM contents change without changing the filename
- The detected save type appears incorrect
- A game stops loading after being modified

Delete the matching file from the `PATCH` folder and launch the ROM again.

---

## Kernel 1.78

Kernel 1.78 was the final major release before the Kernel 2.x Auto Patch Engine series.

### Changes

- Removed the previous limit of 78 files in the root directory
- Retained a limit of 99 files inside individual subfolders for performance

Kernel 1.78 does not include:

- The Auto Patch Engine
- Reusable patch files
- Global Soft Reset and Sleep
- Per-game GSS settings
- EZ-Flash Reform support

Kernel 2.05 is recommended for supported hardware.

---

## Auto Patch Engine

Kernel 2.00 and newer automatically analyze and patch clean GBA ROMs.

The Auto Patch Engine can apply:

- Save-type patches
- SRAM compatibility patches
- Loading adjustments
- Anti-piracy workarounds
- Soft-reset patches
- Sleep-mode patches

Patch data is stored in:

```text
/PATCH/
```

### Regenerating a Patch

1. Turn off the console.
2. Insert the storage card into a computer.
3. Open the `PATCH` folder.
4. Delete the patch associated with the affected ROM.
5. Safely eject the storage card.
6. Launch the ROM again.
7. Allow the first-launch patching process to finish.

Do not reuse an old patch after modifying or replacing its ROM.

---

## GSS Configuration

GSS stands for Global Soft Reset and Sleep.

It modifies a game during loading to provide:

- Return-to-menu soft reset
- Sleep mode
- Customizable hotkeys

Because GSS patches the game, it is not compatible with every commercial game, homebrew application, ROM hack, or translation.

### Possible GSS Compatibility Symptoms

- White screen
- Black screen
- Freezing during startup
- Freezing during gameplay
- Broken controls
- Graphical corruption
- Audio problems
- Sleep mode failing to wake
- Soft reset failing to return to the menu

Launch the affected game with:

`L + B`

This bypasses GSS for that launch.

Use:

`L + SELECT`

when writing a game to NOR without the GSS patch.

---

## Hard-Reset Loading

Some games with anti-piracy checks or unusual startup behavior may require hard-reset loading.

Launch the game with:

`L + A`

Hard-reset loading can also be configured globally through `KEYSET.CFG`.

Use hard-reset loading when a verified clean ROM does not work through the normal `A` launch option.

---

## Save Backup During Startup

The EZ-Flash IV stores the active game save in battery-backed SRAM.

When the kernel starts, it copies the pending SRAM data to the matching file in:

```text
/SAVE/
```

Pressing `L` during kernel startup skips the save-backup process.

Skipping the backup can cause the most recent save progress to be lost or overwritten when another game is launched.

Before updating the kernel:

1. Start the cartridge normally.
2. Do not press `L`.
3. Allow the save backup to finish.
4. Back up the entire `SAVE` folder to a computer.

---

## Custom Kernels and Skins

EZ-Flash IV themes are normally distributed as modified copies of:

`ezfla_up.bin`

Installing a theme therefore installs an entire modified kernel.

Before installing a custom skin:

- Confirm which official kernel version it is based on
- Confirm that it supports the specific EZ-Flash IV hardware revision
- Back up the `SAVE` folder
- Keep a copy of official Kernel 2.05
- Allow any pending SRAM save backup to finish

An older theme can silently downgrade the installed kernel.

Downgrading may remove:

- Auto Patch Engine improvements
- Reusable patch files
- GSS
- Per-game GSS controls
- Reform compatibility
- Later undocumented fixes

Return to official Kernel 2.05 before troubleshooting game-loading, save, or storage-card problems.

---

## Upgrade Warnings

- Allow the pending SRAM save backup to finish before updating.
- Do not press `L` during startup if a save is waiting to be backed up.
- Back up the `SAVE` folder before installing a kernel.
- Do not turn off the console during the update.
- Use a console with a charged battery or reliable external power.
- Delete `ezfla_up.bin` after the update completes.
- Do not install kernels made for the Omega, Omega Definitive Edition, Air, Junior, Parallel, or other EZ-FLASH products.
- Confirm hardware compatibility before installing a custom kernel or theme.
- Do not interrupt NOR writing, deletion, or formatting.
- Do not assume that a themed kernel is based on Kernel 2.05.

The official current download is specifically labeled for the EZ-Flash IV MicroSD. Owners of substantially older or unusual EZ-Flash IV hardware revisions should verify compatibility before installing it.

---

## Known Version Issues

### Kernel 2.00 Repatching

Kernel 2.00 introduced automatic patching but did not yet include the reusable patch-data system described for Kernel 2.01.

Repeated launches may therefore take longer than with Kernel 2.01 and newer.

### Kernel 2.02 GSS Compatibility

Some games cannot use the GSS patch correctly.

Possible symptoms include blank screens, freezing, or failed sleep and soft-reset functions.

Launch the game with `L + B`.

### Kernel 2.03 Configuration

Per-game GSS controls require a correctly configured `KEYSET.CFG` file in the root of the storage card.

Incorrect settings can cause games to launch with unexpected GSS or hard-reset behavior.

### Kernel 2.04 on EZ-Flash IV

Kernel 2.04 primarily added Reform support.

The official announcement allowed EZ-Flash IV owners to remain on Kernel 2.03, indicating that the update was not required specifically for EZ-Flash IV operation.

### Kernel 2.05 Changelog

EZ-FLASH currently provides Kernel 2.05 but does not publish a detailed changelog for it.

Specific fixes should not be attributed to Kernel 2.05 without supporting documentation.

### Old Patch Files

A patch generated for one ROM revision may not work with a different ROM using the same filename.

Delete the old patch and allow the kernel to regenerate it.

### Custom Skins

A custom skin may contain an older kernel.

Installing one can reintroduce old loading behavior or remove newer features.

---

## Basic Troubleshooting

1. Allow the pending save backup to finish.
2. Back up the `SAVE` folder.
3. Install official Kernel 2.05.
4. Remove any custom or themed kernel.
5. Use a correctly formatted and supported storage card.
6. Delete the affected game's old file from the `PATCH` folder.
7. Test with a verified clean GBA ROM.
8. Launch with `L + B` to disable GSS.
9. Launch with `L + A` to test hard-reset mode.
10. Check `KEYSET.CFG` for incorrect global or per-game settings.
11. Test another storage card or card adapter.
12. Clean the cartridge and storage-card contacts.
13. Test the cartridge in another console.

Persistent crashes or memory failures across multiple clean ROMs, cards, and consoles may indicate defective cartridge hardware rather than a kernel problem.

---

## Notes

- Kernel 2.05 is the latest official download.
- The update file is `ezfla_up.bin`.
- The EZ-Flash IV does not use a separately numbered firmware package.
- Kernel 2.00 introduced onboard automatic ROM patching.
- Kernel 2.01 added reusable patch files and faster repeat launches.
- Kernel 2.02 introduced Global Soft Reset and Sleep.
- Kernel 2.03 added global and per-game GSS controls.
- Kernel 2.04 added EZ-Flash Reform support.
- No detailed official Kernel 2.05 changelog is currently published.
- The kernel stores normal save files in the `SAVE` folder.
- Automatically generated ROM patches are stored in the `PATCH` folder.
- Custom themes are distributed as modified kernel installers.
- Keep regular backups of the `SAVE` folder.

---

## Sources

- [Official EZ-FLASH Download Page](https://www.ezflash.cn/download/)
- [Official EZ-Flash IV Quick Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)
- [Kernel 2.00 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-00-released/)
- [Kernel 2.02 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-02-released/)
- [Kernel 2.03 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-03-released/)
- [Kernel 2.04 Announcement](https://www.ezflash.cn/ez4kernel-2-04-released/)
