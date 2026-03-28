# EZ-Flash Omega (DE) Troubleshooting Guide

This section covers common issues with the EZ-Flash Omega Definitive Edition and how to resolve them. Whether you're facing ROM detection problems, save corruption, boot loops, or cheat malfunctions, this guide can help.

---

## ROM Doesn't Show Up

**Causes:**
- Unsupported file type (only `.gba`, `.gb`, `.gbc`, `.nes` supported)
- ROM buried too deep in folder hierarchy
- Special characters in the file name
- Corrupt or incompatible ROM

**Solutions:**
- Store ROMs in `/GBA/`, `/GB/`, `/NES/`, etc.
- Keep folder names short and simple
- Rename ROMs to remove non-alphanumeric characters
- Use clean, verified ROMs only

---

## Save File Not Working or Keeps Resetting

**Causes:**
- Powering off without returning to the kernel menu
- Save type mismatch
- 128KB dual-save games (e.g., Pokémon) not properly handled

**Solutions:**
- Save in-game twice, then return to the EZ-Flash menu
- Confirm a `.sav` is created in `/SAVER/`
- Refer to the [Save Behavior Guide](../Docs/Save.md)

---

## Pokémon "Save is Corrupted" Message

**Why it happens:**  
Pokémon titles use 128KB Flash saves with dual slots. If one slot isn't updated, the game flags the save as corrupt.

**Solutions:**
- Save twice in-game
- Return to the kernel before shutting off
- If needed, delete the `.sav` and restart from a clean state

---

## Game Boots Then Instantly Reboots

**Causes:**
- Bad patch
- Incompatible ROM
- Incorrect save type

**Solutions:**
- Use [GBATA](https://www.romhacking.net/utilities/601/) to clean headers
- Verify ROM integrity before patching
- Reapply patch to a verified ROM

---

## Game Loads to White Screen

**Causes:**
- ROM hack built on FireRed v1.1 (use v1.0 instead)
- Corrupt `.sav` or `.cht` file
- SD card format issues
- Incompatible cheats
- Broken theme or outdated kernel

**Solutions:**
- Use FireRed v1.0 for patches
- Delete `.sav` and `.cht` files
- Format SD to FAT32 with 64KB allocation
- Disable cheats and test again
- Update to latest kernel
- Patch ROM using [NUPS](https://www.romhacking.net/utilities/606/)

---

## Cart Freezes or Game Won't Start

**Causes:**
- Corrupt theme
- Improper SD formatting
- Faulty kernel

**Solutions:**
- Reformat SD (FAT32, 64K allocation)
- Replace theme with default
- Reinstall kernel from [ezflash.cn](https://www.ezflash.cn/download)

---

## Controls Lag or Menu Glitches

**Causes:**
- Buggy custom theme
- Incompatible ROM region

**Solutions:**
- Switch to default `.skn` theme
- Use US-region ROMs
- Update the kernel

---

## Cheat Menu Doesn't Show Up

**Causes:**
- Cheat support disabled
- Missing or mismatched `CHEAT.DB`

**Solutions:**
- Press `Start` > Options > Enable Cheat Support
- Place `CHEAT.DB` in `/CHEAT/`
- Ensure ROM name matches DB entry
- See the [Cheat Guide](../Tutorials/Cheats.md)

---

## Game Freezes or Crashes When Cheats Are On

**Cause:**  
Incompatible or malformed cheat codes.

**Solution:**
- Use RAM-based cheats only
- Avoid raw GameShark or CodeBreaker entries unless properly converted
- Refer to [Cheat Code Conversion](../Tutorials/Cheats.md)

---

## ROM Dumping and Patching Best Practices

**Checklist:**
- ROM ends with `.gba`
- File size is expected (e.g., ~16MB for FireRed)
- Title screen appears normally
- `.sav` file is generated

**Recommended Tools:**

| Task          | Tool |
|---------------|------|
| IPS Patch     | [Lunar IPS](https://www.romhacking.net/utilities/240/) |
| UPS Patch     | [NUPS](https://www.romhacking.net/utilities/606/) |
| Online Patch  | [ROM Patcher JS](https://www.marcrobledo.com/RomPatcher.js/) |
| Header Fix    | [GBATA](https://www.romhacking.net/utilities/601/) |
| Hash Checker  | [Hashtab](https://implbits.com/products/hashtab/) |

---

## Still Need Help?

Open a GitHub issue at:  
https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/issues/new

Include the following:
- Model and revision (e.g., Omega DE Rev B)
- Game title and region
- Kernel version
- Steps already attempted
- Any `.sav` or `.cht` files (if relevant)

---

Following these practices will prevent most issues. Use clean ROMs, proper formatting, and updated files to ensure a stable experience.
