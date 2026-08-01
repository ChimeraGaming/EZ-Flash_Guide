# EZ-Flash Omega Definitive Edition Firmware and Kernel History

## Current Version

- Kernel: 1.06
- Rev A firmware: 5
- Rev B firmware: 7
- Update file: `ezkernelnew.bin`
- Supported hardware markings:
  - `OMEGA DE`
  - `EZODE`

[Official Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Definitive-Edition-Downloads.html)

[Official EZ-FLASH Downloads](https://www.ezflash.cn/download/)

[Official User Manual](https://www.ezflash.cn/omegade-en.pdf)

This page is for the original 2021 Omega Definitive Edition, including its Rev A and Rev B hardware revisions.

It is not for the separate [2026 Omega Definitive Edition B](../GBA/2026_EZ-Flash_Omega_Definitive_Edition_B.md).

---

## Update Instructions

1. Confirm that the cartridge is an original Omega Definitive Edition.
2. Check the back of the board for `OMEGA DE` or `EZODE`.
3. Back up the `SAVER` folder from the microSD card.
4. Download and extract the latest official package.
5. Place `ezkernelnew.bin` in the root of the microSD card.
6. Insert the microSD card into the cartridge.
7. Hold `R` while powering on the console.
8. Do not turn off the console during the kernel or firmware update.
9. Restart the console after the firmware update.
10. Confirm the installed kernel and firmware in the settings menu.

The update package automatically installs the appropriate firmware for Rev A or Rev B hardware.

---

## Version History

| Kernel | Firmware | Changes |
| --- | --- | --- |
| 1.06 | Rev A: 5 / Rev B: 7 | Optimized the NOR flash driver. Rev B Firmware 7 added support for S98 chips with a `020` suffix. |
| 1.05 | Rev A: 5 / Rev B: 7 | Updated the built-in GBC emulator to Jagoomba Color 0.5. |
| 1.04 | Rev A: 5 / Rev B: 6 | Added addon support for Goodboy Galaxy 1.2 and updated FatFs to version 0.15. |
| 1.03 | Rev B: 6 | Fixed graphical corruption and freezing affecting a small batch of Rev B cartridges. |
| 1.03 | Firmware 5 | Fixed EEPROM saves not working correctly on cartridges using certain S71 chips. The kernel itself was unchanged. |
| 1.03 | Firmware 4 | Fixed Dragon Ball Z anti-piracy problems and the Digi Communication 2 save issue. |
| 1.02 | Firmware 3 | Improved stability, fixed random freezing on some consoles, and repaired the NOR problem introduced by Firmware 2. |
| Not separately identified | Firmware 2 | Attempted to improve stability and random freezing but could make NOR unusable. This firmware was revoked. |
| 1.01 | Firmware 1.0 | Patched the built-in Goomba emulator to support GBC rumble games. |

---

## Revision-Specific Firmware

### Rev A

- Uses Firmware 5 with the current package
- Uses the same kernel interface as Rev B
- Identified by the original `OMEGA DE` board marking

### Rev B

- Uses Firmware 7 with the current package
- Added support for additional internal flash-chip revisions
- Received fixes for graphical corruption and freezing on a small hardware batch
- Usually identified by the `EZODE` board marking

Rev B is a hardware revision of the original Definitive Edition. It is not the separate Omega Definitive Edition B released in 2026.

---

## Major Changes by Version

### Kernel 1.06

- Optimized the NOR flash driver
- Intended to improve NOR writing and management reliability

### Firmware 7 for Rev B

- Added support for S98 chips ending in `020`

### Kernel 1.05

- Updated the built-in GBC emulator to Jagoomba Color 0.5

Previously used GBC games may retain settings created by the older Goomba emulator.

When a GBC game has incorrect compatibility settings:

1. Open the emulator menu with `L + R`.
2. Open the additional Game Boy settings.
3. Select `Prefer GBC over SGB`.

### Kernel 1.04

- Added addon support for Goodboy Galaxy 1.2
- Added improved rumble support for the game
- Updated FatFs to version 0.15

### Kernel 1.03 and Firmware 6

- Fixed graphical corruption
- Fixed freezing on a small batch of Rev B cartridges

### Kernel 1.03 and Firmware 5

- Fixed EEPROM save failures involving certain S71 chips
- Required affected users to run the kernel update again so the corrected firmware could install

### Kernel 1.02 and Firmware 3

- Fixed random freezing on some consoles
- Repaired NOR flash made unusable by the revoked Firmware 2 release

---

## Official Version-Label Inconsistency

The official manufacturer page labels the newest package as:

`Kernel 1.06 and Firmware 7.0`

It also includes a Kernel 1.06 changelog entry for the optimized NOR flash driver.

However, older text remaining on the same page states that the installed kernel is `K105`.

This guide records Kernel 1.06 as the current release because that is the current package label and the newest kernel listed in the official changelog.

---

## Upgrade Warnings

- Firmware 2 was revoked because it could make NOR flash unusable.
- Do not install the revoked Firmware 2 package.
- Do not interrupt a kernel, firmware, or NOR operation.
- Confirm whether the cartridge is Rev A or Rev B before troubleshooting.
- Only use `ezkernelnew.bin` made for the original Definitive Edition.
- Do not use `ezbluekernel.bin` from the 2026 Definitive Edition B.
- Do not use `ezkernel.bin` from the original Omega.
- Do not use `ezairkernel.bin` from the Air.
- Back up the `SAVER` folder before updating.

---

## Known Version Issues

### Revoked Firmware 2

Firmware 2 attempted to address freezing but could leave NOR flash unusable.

Kernel 1.02 and Firmware 3 fixed the NOR issue.

### Certain S71 Chips

Some cartridges using specific S71 chips had EEPROM save failures.

Firmware 5 corrected the issue.

### Small Batch of Rev B Cartridges

Some Rev B cartridges experienced:

- Graphical corruption
- Freezing
- Stability problems

Firmware 6 for Rev B addressed these problems.

### GBC Emulator Settings After Kernel 1.05

The switch from Goomba to Jagoomba Color can conflict with settings already stored in older GBC save data.

Set the affected game to `Prefer GBC over SGB` from the emulator settings.

### NOR Problems on Older Versions

Install Kernel 1.06 before diagnosing persistent NOR-writing problems. Kernel 1.06 specifically optimized the NOR flash driver.

---

## Sources

- [Official Omega Definitive Edition Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Definitive-Edition-Downloads.html)
- [Official EZ-FLASH Manufacturer Downloads](https://www.ezflash.cn/download/)
- [Official Omega Definitive Edition Manual](https://www.ezflash.cn/omegade-en.pdf)
