# EZ-Flash Omega Definitive Edition B Firmware and Kernel History

## Current Version

- Kernel: 1.01
- Firmware: 2
- Update file: `ezbluekernel.bin`
- Required hardware marking: `EZODE-B`
- PCB color: Blue

[Official Firmware Download](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Definitive-Edition-B-Downloads.html)

[Official EZ-FLASH Downloads](https://www.ezflash.cn/download/)

The Omega Definitive Edition B is a separate model from the original 2021 Omega Definitive Edition.

The two models do not share kernels or firmware.

---

## Update Instructions

1. Confirm that the cartridge has a blue PCB marked `EZODE-B`.
2. Back up the `SAVER` folder from the microSD card.
3. Download and extract the latest Definitive Edition B package.
4. Place `ezbluekernel.bin` in the root of the microSD card.
5. Insert the microSD card into the cartridge.
6. Hold `R` while powering on the console.
7. Do not turn off the console during the kernel or firmware update.
8. Restart the console after the update.
9. Confirm the installed versions in the settings menu.

Only use `ezbluekernel.bin` made specifically for the Omega Definitive Edition B.

---

## Version History

| Kernel | Firmware | Changes |
| --- | --- | --- |
| 1.01 | 2 | Addressed problems with 32MB and 64MB movie ROMs, improved NOR compatibility on modified GBA systems, and fixed an FC or NES emulator exit problem. |
| 1.00 | 1.0 | Initial factory release. |

---

## Kernel 1.01 and Firmware 2

This was the first update following the initial factory release.

### Movie ROM Compatibility

- Addressed an issue involving 32MB and 64MB GBA movie ROMs

### NOR Compatibility

- Improved NOR flash compatibility on modified GBA systems

### FC and NES Emulator Exit

- Fixed a problem that could occur when exiting an FC or NES ROM

`FC` refers to the Famicom version of the built-in NES emulator support.

---

## Firmware Compatibility

The Definitive Edition B uses:

`ezbluekernel.bin`

The original 2021 Definitive Edition uses:

`ezkernelnew.bin`

These files are not interchangeable.

Do not install:

- Original Omega `ezkernel.bin`
- Original Definitive Edition `ezkernelnew.bin`
- Air `ezairkernel.bin`

---

## Upgrade Warnings

- Confirm that the board is blue and marked `EZODE-B`.
- Do not identify the cartridge only by the front label or shell.
- Do not install original Definitive Edition firmware.
- Do not interrupt the kernel or firmware update.
- Do not interrupt NOR writing, deletion, or formatting.
- Back up the `SAVER` folder before updating.
- Use a charged console or a reliable external power source.
- Existing custom kernels for the original Definitive Edition are not compatible.

---

## Known Version Issues

### Initial Kernel 1.00 and Firmware 1.0

The first update addressed problems involving:

- 32MB and 64MB movie ROMs
- NOR use on modified GBA systems
- Exiting FC or NES games

Users experiencing these problems should install Kernel 1.01 and Firmware 2.

### Original Definitive Edition Firmware

Installing `ezkernelnew.bin` from the original Definitive Edition will not update the Definitive Edition B correctly.

Use only `ezbluekernel.bin`.

### Limited Update History

The Definitive Edition B is a newer model and currently has only two documented official releases:

- Kernel 1.00 and Firmware 1.0
- Kernel 1.01 and Firmware 2

Additional entries should only be added when an official changelog is published.

---

## Sources

- [Official Definitive Edition B Download Page](https://www.ezflashomega.com/pages/EZ-Flash-Omega-Definitive-Edition-B-Downloads.html)
- [Official EZ-FLASH Manufacturer Downloads](https://www.ezflash.cn/download/)
