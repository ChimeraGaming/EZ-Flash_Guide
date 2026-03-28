# EZ-Flash Versions & Save Behavior Comparison

EZ-Flash carts handle **SAV (save file) behavior** differently based on the model, hardware revision, and save type used by the ROM (e.g., 128KB Flash, EEPROM, etc.). This section breaks it all down - pairing similar carts and identifying known quirks with save handling.

---

## Save Types in GBA Games

Different GBA games use different save technologies:

| Save Type   | Typical Use                          | Save File Size |
|-------------|--------------------------------------|----------------|
| SRAM        | Early/indie GBA games                | 32KB           |
| EEPROM      | Some Nintendo-published titles       | 512B - 8KB     |
| Flash 64K   | Many standard GBA games              | 64KB           |
| Flash 128K  | Pokémon, Boktai, Golden Sun, etc.    | 128KB          |
| FRAM        | Used only in newer flashcarts (e.g., Omega DE) | Varies |

**Note:** Flash 128K is the most complex and important to know - Pokémon uses two save slots inside that space (primary + backup), which can cause issues if not handled properly.

---

## SD Card Format Types & Compatibility

| Format Type | SD Card Size        | Notes                                                                 |
|-------------|---------------------|-----------------------------------------------------------------------|
| FAT32       | Up to 32GB          | Native support in Windows. Most stable format for EZ-Flash carts.     |
| FAT32       | 64GB - 256GB+       | Requires tools like GUIFormat. Use 64K allocation size for best results. |
| exFAT       | 64GB - 1TB          | May boot but prone to save/load errors. Not officially supported.     |
| NTFS        | Any size            | Not recognized by EZ-Flash firmware. Do not use.                      |
| FAT16       | 2GB or less         | Very old format. Can be used, but not recommended. Limited capacity.  |

Use your OS's formatting tool or [SD Card Formatter](https://www.sdcard.org/downloads/formatter/).

---

## EZ-Flash Versions & How They Handle Saves

### EZ-Flash Advance
- Built-in NOR flash.
- Save transferred manually via USB linker on PC.
- No microSD; requires external software.

### EZ-Flash IV / Reform
- PSRAM to SD flow.
- Save is not committed to SD until reboot or soft reset.
- If powered off after saving, progress may be lost.
- Struggles with some 128K save games without patches.

### EZ-Flash Omega
- Saves are held in temporary RAM and committed to SD:
  - On soft reset,
  - On reboot,
  - Or when returning to the menu.
- 128K saves supported, but still follow safe shutdown habits.

### EZ-Flash Omega DE

**Rev A**
- FRAM allows instant in-game saving.
- Reliable with Pokémon and dual-save systems.

**Rev B**
- FRAM chip behaves differently.
- Save corruption can occur in 128K save games unless:
  - You save twice in-game.
  - Or return to the menu to trigger backup.

---

## Other Models

- **EZ-Flash 3in1**: No automatic backup; requires manual save dumping via DS tools.
- **EZ-Flash Junior**: SRAM only writes to SD on reboot or menu return. Powering off too quickly can lose data.

---

## What Happens When a Save File Is Corrupted or Lost?

If a save file becomes corrupted, unreadable, or accidentally deleted (e.g., due to improper shutdown, power loss, or faulty SD card):

- EZ-Flash attempts to fall back to the last known backup:
  - Might be stored in FRAM (Omega DE),
  - Or was last committed to the SD card (Omega, IV, Reform, Junior).

If your save wasn't recently committed (via menu, soft reset, or reboot), it may be hours or even days old.

### Common Triggers for Lost Progress

- Powering off too quickly after saving (especially with Junior, IV, or Reform).
- Forgetting to soft reset or return to the menu.
- Unstable or damaged SD cards.
- Improper eject/removal of SD card without safely dismounting.

### What You Can Do

- Save twice in critical games like Pokémon (Rev B).
- Return to menu or reset after saving.
- Back up your `SAVER/` folder manually every few sessions.
- If you suspect corruption, check `.SAV` file size and last modified timestamp to confirm.

---

## Best Practices (All Models)

- Wait 15 seconds after saving (Pokémon: save twice then wait) before turning off or returning to menu.
- Use tools like GBATA to confirm save type.
- Always return to the kernel menu before powering off (not strictly required on Omega).
- Regularly back up your SD card externally.
- Update firmware for the latest stability improvements.

---

## Directory Structure Affects Save Detection

EZ-Flash devices - especially the Omega and Omega DE - expect ROMs to be stored in shallow, consistent folder paths. If ROMs are buried too deep, save files may not be detected, or the cart may fail to load the game entirely.

### Problem Example

```
/Roms/GBA/Pokemon/Completed/Beta/Game.gba
```

- This path is too deep.
- The save file (`.sav`) might fail to be created or loaded correctly.
- Games may "start fresh" every time or show save corruption.

### Recommended Folder Layout

```
/GBA/Game.gba
```

or

```
/Game.gba
```

- Keeps paths short and simple.
- Ensures that `.sav` files are placed correctly inside `/SAVER/` or backed up properly by the firmware.
- Compatible with all themes and save types.

The deeper the file, the more likely save detection fails. Some themes or kernels may handle deep folders better, but to guarantee compatibility - keep your ROMs no deeper than 1-2 folders down from root.

Refer to the [Directory Structure Guide](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Docs/Directory_Structure.md) for visual examples and best practices.
