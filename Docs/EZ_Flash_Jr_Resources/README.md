# nitro2k01's SGB Enabler for EZ-Flash Jr.

**Posted:** August 19, 2021  
**Source:** [GG8 Blog Post](https://blog.gg8.se/wordpress/2021/08/19/nitro2k01s-sgb-enabler-for-ez-flash-jr/)

---

## What It Does

- A patched kernel (v1.04e) for EZ-Flash Jr that enables Super Game Boy (SGB) support.
- Fixes the issue where SGB couldn't detect the EZ-Flash Jr cart (resulting in a black screen).
- Fully restores borders, color palettes, and enhanced SGB sound.

---

## How It Works

- The default EZ-Flash Jr briefly resets the Game Boy CPU during boot.
- This patch replays the necessary boot ROM calls so the SNES correctly detects the cartridge.
- No hardware mod required - just replace `ezgb.dat`.

---

## Compatibility

- Works on:
  - Super Game Boy 1 (SGB1)
  - Super Game Boy 2 (SGB2)
  - PAL/NTSC SNES systems
  - Some SNES clones
- Also runs on DMG/GBC, though:
  - Increases boot time (due to SGB check).
  - Easily revert to stock kernel if undesired.

---

## Installation Instructions

1. Backup your current `ezgb.dat` file.
2. Download and extract the patched file: `kernel104-sgbenabler.zip`.
3. Place the new `ezgb.dat` on your SD card root.
4. Insert the EZ-Flash Jr into your SGB/SNES.
5. Power on - no reset needed.

---

## Notes & Feedback

- Safe and reversible - does not modify firmware.
- Minor visual glitches reported by a few users (resolved with reset).
- Great compatibility across SGB models and SNES regions.
- Increased boot time on non-SGB systems is the only drawback.

---

## Links

- [Download SGB Enabler](https://blog.gg8.se/wordpress/wp-content/uploads/kernel104-sgbenabler.zip)
- [Original Blog Post](https://blog.gg8.se/wordpress/2021/08/19/nitro2k01s-sgb-enabler-for-ez-flash-jr/)

---

**TL;DR:** This patch gives EZ-Flash Jr full Super Game Boy functionality with no mods, restores visual/audio enhancements, and is 100% safe to use or revert.
