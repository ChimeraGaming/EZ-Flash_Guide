# Editing Save Files

Learn how to safely extract, edit, and reinsert save files (`.sav`) for use with the EZ-Flash Omega Definitive Edition and other GBA/GB carts. Whether you're modifying items, unlocking events, or fixing a corrupted save, this guide walks you through it.

---

## Where Save Files Are Stored

On the microSD, look inside the `/SAVER/` folder.  
Each file follows this format:

```
/SAVER/GameName.sav
```

- `.sav` files are typically 64KB or 128KB  
- Pokémon and some larger games use 128KB dual-slot saves  
- Save files are automatically backed up by the kernel after powering off properly

---

## Important Save Workflow

Before removing the SD card from your cart:

1. Save in-game TWICE, waiting at least 5 seconds between saves (especially in Pokémon and large games).
2. Return to the kernel menu (via in-game addon or soft reset).
3. Wait for the auto-backup to complete (you'll see "Saving... Do not turn off").
4. Power off the device.
5. Only then remove the SD card and insert it into your PC.

Skipping this process can result in a blank or overwritten `.sav` file.

---

## Tools for Editing `.sav` Files

| Tool | Platform | Best For |
|------|----------|----------|
| [PKHeX](https://projectpokemon.org/home/files/file/1-pkhex/) | Windows | Pokémon GBA/DS save editing |
| [A-Save](https://projectpokemon.org/home/forums/topic/27119-a-save-3rd-generation-save-editor/) | Windows | Gen III Pokémon box & event edits |
| [GBA Tool Advance (GBATA)](https://www.romhacking.net/utilities/601/) | Windows | Header cleaning and save-type inspection |
| [VBA-M](https://github.com/visualboyadvance-m/visualboyadvance-m) | Windows/macOS/Linux | Emulator + save exporting |
| [mGBA](https://mgba.io/) | All platforms | Emulator + debug tools |
| [Hex Editor Neo](https://www.hhdsoftware.com/free-hex-editor) | Windows | Manual edits (advanced users only) |

---

## PKMDS or PKHeX Save File Errors

You may see this error:

> "The selected save file is invalid. If this save file came from a ROM hack, it is not supported. Otherwise, try saving in-game and re-exporting / re-uploading the save file."

### Fixes:

- For ROM hacks: Most editors do not support custom headers or save structures used in hacks. These saves are often incompatible with PKMDS/PKHeX.
- Try resaving in-game twice and allow proper export as described above.
- Convert the save to match expected format using this online tool:  
  [Save File Converter (GBA/NDS/MiSTer)](https://savefileconverter.com/#/mister)

---

## How to Edit a Save

1. Complete the in-game save process (see above).
2. Insert the SD card into your PC.
3. Navigate to `/SAVER/` and find your `.sav`.
4. Make a backup copy - rename it to `Game_backup.sav`.
5. Open the file in a supported save editor (see tools above).
6. Make your changes, then save/overwrite the `.sav` file.
7. Reinsert the SD into your cart and launch the game to verify.

---

## Common Pitfalls

- Game shows "corrupted save": The cart expects valid checksum or dual-slot sync. Use PKHeX or in-game saves to revalidate.
- Wrong save size: Some games use 64KB while others (Pokémon, Boktai) require 128KB. If unsure, check with GBATA.
- Save edits not appearing: Make sure you replaced the correct `.sav`, followed the full save flow, and used compatible tools. (Could have been overwritten when loading up EZ-Flash if you skipped this step before)

---

## Advanced: Extracting Saves from NOR

If the game was flashed to NOR memory, your save might be stuck in internal SRAM.  
To retrieve it:

1. Boot the NOR game, then immediately return to the kernel.
2. The cart will auto-dump the current SRAM save into `/SAVER/`.

---

## Safety Tips

- Never remove the SD card while powered on
- Save twice and return to menu before powering off
- Always keep a backup of `.sav` before editing
- Test edits in an emulator before using on hardware
- Avoid editing ROM hack saves unless you're familiar with their custom structure

---

Return to: [Tutorials Index](./README.md)
