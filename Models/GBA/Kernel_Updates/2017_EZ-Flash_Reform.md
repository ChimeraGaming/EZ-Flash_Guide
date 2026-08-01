# EZ-Flash Reform Kernel History

## Current Version

- Kernel: 2.05
- Update file: `ezfla_up.bin`
- Shared kernel family: EZ-Flash IV MicroSD and EZ-Flash Reform
- Firmware version: Not listed separately

[Official Kernel Download](https://www.ezflash.cn/download/)

[Official EZ4 and Reform Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)

This page covers the EZ4Kernel releases compatible with the EZ-Flash Reform.

The Reform uses the same kernel family as the EZ-Flash IV MicroSD. Kernel 2.04 was the first release specifically updated to support the Reform.

---

## Update Instructions

1. Back up the `SAVER` folder from the microSD card.
2. Download and extract EZ4Kernel 2.05.
3. Place `ezfla_up.bin` in the root of the microSD card.
4. Insert the microSD card into the Reform.
5. Hold `R` while powering on the console.
6. Keep the console powered until the update finishes.
7. Confirm that version `2.05` appears in the upper-right corner of the menu.
8. Delete `ezfla_up.bin` from the microSD card after the update.

Do not turn off the console while the kernel is being installed.

---

## Version History

| Kernel | Changes |
| --- | --- |
| 2.05 | Additional game and ROM compatibility improvements. This is the final official Reform-compatible release. |
| 2.04 | Added support for the newly released EZ-Flash Reform hardware. |
| 2.03 | Added a global GSS switch and individual per-game GSS controls through `KEYSET.CFG`. Improved soft-reset and sleep compatibility. |
| 2.02 | Added Global Soft Reset and Sleep, known as GSS. Added customizable soft-reset and sleep hotkeys through `KEYSET.CFG`. |
| 2.01 | Improved the Auto Patch Engine to reduce initial loading times. Added additional anti-piracy and game-compatibility patches. |
| 2.00 | Added the onboard Auto Patch Engine. Clean GBA ROMs could now be copied directly to the microSD card and patched by the kernel when launched. |
| 1.78 | Removed the previous limit of 78 files in the root directory. Subdirectories remained limited to 99 files for performance. |

No detailed public changelog is currently preserved for every internal compatibility change made between these releases.

---

## Kernel 2.05

Kernel 2.05 is the final official kernel for the Reform.

### Changes

- Additional game compatibility improvements
- Additional ROM patching improvements
- Retains Reform hardware support introduced in Kernel 2.04
- Retains the Auto Patch Engine
- Retains configurable soft reset and sleep

The published changelog does not identify every game or patch changed in this release.

---

## Kernel 2.04

Kernel 2.04 added support for the EZ-Flash Reform.

Earlier EZ4Kernel releases were designed for EZ-Flash IV hardware and should not be treated as complete Reform releases.

### Changes

- Added EZ-Flash Reform hardware support
- Retained compatibility with supported EZ-Flash IV MicroSD models
- Retained automatic ROM patching
- Retained GSS soft-reset and sleep functions

Kernel 2.04 is the earliest version that should normally be installed on a Reform.

---

## Kernel 2.03

Kernel 2.03 expanded the Global Soft Reset and Sleep system introduced in Kernel 2.02.

### Changes

- Added a global GSS enable or disable setting
- Added individual per-game GSS controls
- Added GSS configuration through `KEYSET.CFG`
- Improved soft-reset compatibility
- Improved sleep-mode compatibility

The per-game setting allows GSS to remain enabled globally while being disabled for games that freeze or fail when patched.

---

## Kernel 2.02

Kernel 2.02 introduced Global Soft Reset and Sleep.

### Default Hotkeys

| Function | Default Hotkey |
| --- | --- |
| Return to the EZ4 menu | `L + Up + B` |
| Enter sleep mode | `L + R + Start` |
| Wake from sleep | `Start + Select` |

The controls can be changed through the `KEYSET.CFG` file in the root of the microSD card.

### Game-Loading Controls

| Function | Hotkey |
| --- | --- |
| Load normally | `A` |
| Load using hard reset | `L + A` |
| Load without GSS | `L + B` |
| Write to NOR normally | `SELECT` |
| Write to NOR without GSS | `L + SELECT` |

Some games do not work correctly with GSS enabled. Use `L + B` to launch those games without the soft-reset and sleep patch.

---

## Kernel 2.01

Kernel 2.01 improved the Auto Patch Engine introduced in Kernel 2.00.

### Changes

- Reduced the time required to patch games
- Reduced later loading times by reusing stored patch data
- Added additional anti-piracy patches
- Added additional game-compatibility fixes

The first launch of a game may still take longer because the kernel must analyze and patch the ROM.

Later launches use the patch data stored in the `PATCH` folder.

---

## Kernel 2.00

Kernel 2.00 introduced the onboard Auto Patch Engine.

### Changes

- Added automatic save-type patching
- Added automatic ROM compatibility patching
- Allowed clean GBA ROMs to be copied directly to the microSD card
- Created reusable patch data during the first launch
- Stored generated patch data in the `PATCH` folder

Generated patches are stored in:

`/PATCH/`

The first launch of a game takes longer while the patch is generated. Later launches are faster because the existing patch is reused.

If a ROM is replaced with a different revision or a newly patched version, delete its existing patch file so the kernel can generate a new one.

---

## Kernel 1.78

Kernel 1.78 was released before the Reform but is an important part of the shared EZ4Kernel history.

### Changes

- Removed the previous limit of 78 files in the root directory
- Retained a limit of 99 files inside individual folders for menu-performance reasons

Kernel 1.78 does not contain official Reform hardware support.

Use Kernel 2.05 on the Reform.

---

## Auto Patch Engine

Kernel 2.00 and newer automatically patch clean GBA ROMs when they are first launched.

The kernel may apply:

- Save-type patches
- SRAM compatibility patches
- Anti-piracy fixes
- Loading adjustments
- Soft-reset and sleep patches

Patch data is stored separately from the original ROM.

When troubleshooting a game:

1. Delete its existing file from the `PATCH` folder.
2. Confirm that the ROM is clean and unmodified.
3. Launch the game again and allow the patch to be regenerated.
4. Use `L + B` if the game does not work with GSS.
5. Use `L + A` if the game requires hard-reset loading.

---

## GSS Compatibility

GSS stands for Global Soft Reset and Sleep.

It patches the game to provide:

- Return-to-menu soft reset
- Sleep mode
- Configurable hotkeys

Because GSS modifies the game during loading, it is not compatible with every commercial game, ROM hack, or translation.

Symptoms of GSS incompatibility can include:

- White screen
- Black screen
- Freezing after launch
- Freezing during gameplay
- Broken controls
- Sleep mode failing to wake
- Soft reset failing to return to the menu

Launch the game with `L + B` to test it without GSS.

---

## Custom Kernels and Skins

Reform and EZ-Flash IV themes are compiled into modified copies of:

`ezfla_up.bin`

A theme is therefore also a complete kernel installer.

Before installing a custom skin:

- Confirm that it is based on Kernel 2.05
- Confirm that it supports EZ-Flash Reform
- Back up the `SAVER` folder
- Keep a copy of the official Kernel 2.05 installer

An older theme may install an older kernel and remove Reform support, Auto Patch Engine improvements, or compatibility fixes.

Return to the official Kernel 2.05 before troubleshooting game-loading or save problems.

---

## Upgrade Warnings

- Only use a kernel confirmed to support the Reform.
- Do not install Omega, Omega Definitive Edition, Air, Junior, or Parallel kernels.
- Do not turn off the console during the update.
- Use a console with a charged battery or reliable external power.
- Back up the `SAVER` folder before updating.
- Allow any pending SRAM save to be copied to the microSD card before updating.
- Delete `ezfla_up.bin` after the update to prevent accidental reinstallations.
- Do not install an older custom skin unless it is based on Reform-compatible Kernel 2.04 or 2.05.

---

## Known Kernel Issues

### GSS Compatibility

Some games do not work correctly with soft reset or sleep enabled.

Launch the affected game with:

`L + B`

### Automatic Patching

Modified ROMs, ROM hacks, translations, and unusual save types may not be detected correctly.

Delete the existing patch file and allow the kernel to process the ROM again.

### First-Launch Loading Time

The first launch may take considerably longer because the Auto Patch Engine must analyze the ROM and create its patch file.

This is normal.

### Old Patch Files

A patch generated for an older ROM revision may not work with a replacement ROM using the same filename.

Delete the old entry from the `PATCH` folder after replacing or modifying a ROM.

### Older Custom Skins

Installing a skin based on an older kernel can:

- Remove Reform compatibility
- Remove GSS improvements
- Reintroduce older compatibility problems
- Prevent the cartridge from loading correctly

Use skins based on Kernel 2.05.

### File and Folder Limits

Kernel 1.78 removed the previous 78-file root limit, but folders remain limited to approximately 99 visible files for performance.

Organize large ROM libraries into multiple folders.

---

## Basic Troubleshooting

1. Install official Kernel 2.05.
2. Remove any older custom kernel or skin.
3. Use a FAT32-formatted microSD card no larger than 32GB.
4. Back up and remove old files from the `PATCH` folder.
5. Test with a verified clean ROM.
6. Launch the game with `L + B` to disable GSS.
7. Try `L + A` for hard-reset loading.
8. Confirm that the current save has been backed up before testing other games.
9. Clean the cartridge and microSD contacts.
10. Test another reputable microSD card.
11. Test the Reform in another console.

---

## Notes

- The Reform shares its kernel family with the EZ-Flash IV MicroSD.
- Kernel 2.04 introduced official Reform support.
- Kernel 2.05 is the final official release.
- The update filename is `ezfla_up.bin`.
- The Reform does not use a separately numbered firmware package.
- Kernel 2.00 introduced automatic onboard ROM patching.
- Kernel 2.02 introduced soft reset and sleep.
- Kernel 2.03 added global and per-game GSS controls.
- Custom themes are compiled into modified kernel installers.
- Keep regular backups of the `SAVER` folder.

---

## Sources

- [Official EZ-FLASH Download Page](https://www.ezflash.cn/download/)
- [Official EZ4 and Reform Tutorial](https://www.ezflash.cn/ez4quicktutorial.html)
- [Official Kernel 2.03 Announcement](https://www.ezflash.cn/ez-flash-iv-kernel-2-03-released/)
