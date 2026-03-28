# Creating Thumbnails for Omega DE 

This guide walks you through creating and using **game thumbnails** on your EZ-Flash Omega Definitive Edition.

[Jump to GBC/GB Thumbnail Guide](#bonus-creating-gbcgb-multi-rom-thumbnails-goomba-method)

---

## What Are Thumbnails?

Thumbnails are `.bmp` images that appear beside your ROMs in the game browser. They make your flashcart look like a modern game menu.

---

## Thumbnail Requirements

| Property     | Value                        |
|--------------|------------------------------|
| File Format  | `.bmp` (bitmap)              |
| Dimensions   | **120x80 pixels**            |
| Color Depth  | **24-bit (RGB)**             |
| File Name    | Must match the **4-letter Game ID** (e.g., `BPRE.bmp`) |
| Folder       | Stored inside `/IMGS/` subfolders based on Game ID |

---

## Finding or Making a 4-Letter Game ID

The **Game ID** is what the EZ-Flash kernel uses to match thumbnails. For official games, you can extract this code from the ROM header. For ROM hacks, you can **create your own custom ID** using **RHEA**.

### Official ROMs

Use [GBATA](https://www.romhacking.net/utilities/601/) or [RHEA](https://www.romhacking.net/utilities/542/) to find the **Game Code** (4-letter serial) from your ROM.

Example:
- FireRed v1.0 uses `BPRE`
- Metroid Fusion uses `AMTE`

### ROM Hacks: Custom Game IDs with RHEA

Use [RHEA](https://github.com/sterophonick/rhea) to assign a custom Game Code:

> RHEA Folder Bug Warning  
> If multiple `.gba` files are in the same folder, RHEA may rename all of them to match the first ROM's Game ID.  
> To avoid this:
> - Place each `.gba` file in its own folder before opening with RHEA  
>   - Suggested: `/Thumbnails/Needs Formatting/Game Name/GameName.gba`  
> - Change folders between games if doing multiple edits  
> - Close and reopen RHEA after each ROM  
> - After renaming, move each `.gba` into a clean `/Formatted/` folder to help with next steps.

---

## Recommended Tools

- [EZ Omega Thumbmaker](https://gbatemp.net/threads/creating-your-own-thumbnails-for-the-ez-flash-omega-firmware.510210/) - Auto-format images  
- [Paint.NET](https://www.getpaint.net/) or [GIMP](https://www.gimp.org/) - Manual BMP editing  
- [RHEA](https://www.romhacking.net/utilities/542/) - View and edit ROM Game IDs  
- [GBATA](https://www.romhacking.net/utilities/601/) - Legacy tool to inspect ROMs

---

## Auto Method (Thumbmaker)

1. Open **EZ Omega Thumbmaker**
2. Load an image (cover art or screenshot)
3. It resizes to 120x80 BMP automatically
4. Rename the BMP to the Game ID (e.g., `ODYS.bmp`)
5. Place it in the proper `/IMGS/` subfolder (see next section)

---

## Final File & Folder Structure

Once your thumbnail is complete:

- The filename must be `XXXX.bmp` where `XXXX` is the 4-letter Game ID (all caps)
- It must be placed into a folder path based on its serial, like so:

```
/IMGS/B/P/BPRE.bmp    # Game ID BPRE  
/IMGS/O/D/ODYS.bmp    # Game ID ODYS  
/IMGS/U/N/UNBD.bmp    # Game ID UNBD
```

> If the folders don't exist, create them manually. All folder names and file names must be UPPERCASE.

---

## Example Setup Table

| Game Title           | Game Code | ROM File               | Thumbnail Path         |
|----------------------|-----------|------------------------|------------------------|
| Pokémon FireRed      | `BPRE`    | `Pokemon_FireRed.gba`  | `/IMGS/B/P/BPRE.bmp`   |
| Pokémon Unbound      | `UNBD`    | `Pokemon_Unbound.gba`  | `/IMGS/U/N/UNBD.bmp`   |
| Pokémon Odyssey      | `ODYS`    | `Pokemon_Odyssey.gba`  | `/IMGS/O/D/ODYS.bmp`   |

---

## Bonus: Creating GBC/GB Multi-ROM Thumbnails (Goomba Method)

You can compile One or Multiple Game Boy or Game Boy Color ROMs into a single `.gba` file using **Goomba Front**, then assign a custom Game ID for thumbnail compatibility.

### Goomba Front Steps

Steps in visual order from top to bottom of the window.

1. Select Emulator File  
   Choose `goomba.gba` (provided with Goomba Front)

2. Select Output File  
   Choose where to save the compiled `.gba` file and name it appropriately (e.g., `ZeldaSeasons.gba`)

3. Add GB/GBC Games  
   Browse and add `.gb` or `.gbc` files  
   - Add one or multiple  
   - Right-click the title on the right panel to rename its Game Serial (this is the Game ID used for thumbnails)

4. Click Compile

---

### Thumbnail for Goomba `.gba`

- Must be a **40x56**, **8-bit** uncompressed BMP
- File name must match the compiled `.gba` file:
  ```
  ZeldaSeasons.gba
  ZeldaSeasons.bmp
  ```

Place both on your SD card in the same folder.

---

### Modify & Verify Header/Serial in Hex Editor (Use this instead of RHEA as it will break the gba file and load up white)

Open the `.gba` file in HxD or GBATA and verify: (Usually Line 11)

| Field         | Offset     | Example (`ZROA`)         |
|---------------|------------|--------------------------|
| Game Title    | `0xA0-0xAB`| `ZELDA ROA   ` (12 bytes padded with spaces) |
| Game Code     | `0xAC-0xAF`| `ZROA`                   |
| Maker Code    | `0xB0-0xB1`| `01` (Nintendo)          |
<img width="679" height="309" alt="image" src="https://github.com/user-attachments/assets/0e64c737-afcd-4966-9c16-4a4e3941d242" />

---

### Testing on EZ-Flash DE

1. Boot the flashcart
2. Press SELECT to toggle Thumbnail View
3. Your Goomba `.gba` file will now show its thumbnail
4. Launching it should open the Goomba menu with your GBC/GB ROMs or Direct if you only did 1 Game (Recommended for multiple Thumbnails)

---

## HEX Table Guide

When modifying ROM headers manually (for Game Titles or Game Codes), you need to convert letters and numbers into hex bytes.

Use this full ASCII/HEX reference:

[https://www.asciitable.com/](https://www.asciitable.com/)

## Successful GBC Thumbnail
![466581790-c8a6cf16-fb3e-4afa-baad-aa91a47c8c7e_50](https://github.com/user-attachments/assets/6e491d40-5f12-4bf0-a411-7c3c8dbb85eb)

---
