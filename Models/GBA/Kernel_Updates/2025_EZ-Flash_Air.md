# EZ-Flash Air Firmware and Kernel History

## Current Version

- Kernel: 1.05
- Firmware: 4
- Update file: `ezairkernel.bin`

[Official Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Air-Downloads.html)

[Official EZ-FLASH Downloads](https://www.ezflash.cn/download/)

[Official User Manual](https://www.ezflash.cn/air.pdf)

---

## Update Instructions

1. Back up the `SAVER` folder from the microSD card.
2. Download and extract the latest official Air package.
3. Place `ezairkernel.bin` in the root of the microSD card.
4. Insert the microSD card into the Air.
5. Hold `R` while powering on the console.
6. Do not turn off the console during the kernel or firmware update.
7. Restart the console after the update.
8. Confirm the installed versions in the settings menu.

Only use `ezairkernel.bin` made specifically for the EZ-Flash Air.

---

## Version History

| Kernel | Firmware | Changes |
| --- | --- | --- |
| 1.05 | 4 | Redesigned NOR management. Added individual ROM deletion, reusable freed space, real-time NOR usage information, and improved ROM writing and reading compatibility. |
| 1.04 | 3 | Fixed RTC support in Mode B and improved support for certain iQue games. |
| 1.02 | Not separately identified | Fixed a rare bug triggered when addon functions were enabled. |
| 1.01 | Not separately identified | Fixed an incorrect ESV save type created with addons enabled, improved GBC emulator usability, and added 256KB alignment for non-standard ROM sizes. |

The official changelog does not contain a separate Kernel 1.03 entry.

---

## Major Changes by Version

### Kernel 1.05 and Firmware 4

NOR management was redesigned.

Changes include:

- ROMs can be deleted individually
- ROMs no longer have to be deleted from the last entry backward
- Freed NOR space can be reused
- Current NOR usage can be checked in real time
- Improved ROM-writing compatibility
- Improved ROM-reading compatibility

### Required First Use After Updating

After installing Firmware 4 and Kernel 1.05:

1. Open the NOR menu.
2. Format NOR or completely delete all existing ROMs.
3. Write the ROMs back to NOR.

The official instructions require a complete NOR erase before the first use of the redesigned management system.

### Kernel 1.04 and Firmware 3

- Fixed Real-Time Clock support while using Mode B
- Improved support for certain iQue GBA releases

### Kernel 1.02

- Fixed a rare bug caused by enabling addon functions

### Kernel 1.01

- Fixed an incorrect ESV save type generated when addons were enabled
- Improved the built-in GBC emulator interface
- Added automatic 256KB alignment for ROMs with non-standard capacities

The alignment change prevents one unusually sized ROM from interfering with ROMs written after it.

---

## Upgrade Warnings

- Format or completely erase NOR after installing Kernel 1.05 and Firmware 4.
- Do not reuse the old NOR layout without erasing it first.
- Back up normal save files before updating.
- Do not interrupt the kernel or firmware update.
- Do not interrupt NOR writing, deletion, or formatting.
- Only use Air-specific firmware.
- Do not install Omega, Omega Definitive Edition, or Definitive Edition B kernels.
- Use a charged console or a reliable external power source.

---

## Known Version Issues

### Old NOR Layout After Kernel 1.05

ROMs written under an older version may not work correctly with the redesigned Firmware 4 NOR manager.

Completely erase NOR before writing games after the update.

### Mode B RTC Before Kernel 1.04

Earlier versions had incorrect or incomplete RTC behavior while operating in Mode B.

Kernel 1.04 and Firmware 3 corrected this.

### Addon Bug Before Kernel 1.02

A rare bug could occur when addon functions were enabled.

Kernel 1.02 corrected the problem.

### Incorrect ESV Save Type

The initial kernel could generate an incorrect ESV save type when addons were enabled.

Kernel 1.01 corrected the save-type handling.

### Non-Standard ROM Sizes

Before the alignment update, a ROM with a non-standard capacity could interfere with ROMs written behind it in NOR.

Kernel 1.01 added automatic 256KB alignment.

---

## Missing Public Version Numbers

The official changelog currently lists:

- Kernel 1.01
- Kernel 1.02
- Kernel 1.04 with Firmware 3
- Kernel 1.05 with Firmware 4

No separate Kernel 1.03 changelog has been published.

This guide does not assign undocumented changes to Kernel 1.03.

---

## Sources

- [Official EZ-Flash Air Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Air-Downloads.html)
- [Official EZ-FLASH Manufacturer Downloads](https://www.ezflash.cn/download/)
- [Official EZ-Flash Air User Manual](https://www.ezflash.cn/air.pdf)
