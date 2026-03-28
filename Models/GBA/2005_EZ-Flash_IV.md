# EZ-Flash IV (2005)

The **EZ-Flash IV** is a popular and long-supported GBA flash cartridge that introduced microSD card support, making it a major step forward from the NOR-based EZ-Flash Advance and EZ-Flash III.

---

## Key Features

- microSD support (up to 2GB for FAT16, unofficial SDHC up to 32GB with newer firmware)  
- Real GBA hardware support (Game Boy Advance, GBA SP)  
- Soft Reset & In-Game Reset (IGR)  
- Cheat Code support (via modified database)  
- Skinning / Theme Support  
- Save support using SRAM (requires soft reset or shutdown to flush save to microSD)  
- NDS Lite Slot-2 support (can be used alongside Slot-1 carts for GBA loading)  
- Supports EZClient PC software for ROM patching  

---

## Limitations

- Requires patching all ROMs via EZClient before copying to SD  
- No RTC (Real-Time Clock) - Games like Pokémon Ruby/Sapphire will run but won't track time-based events  
- Save files not automatically written to SD - must use soft reset or power down to store SRAM to file  
- No NOR flash - games are loaded into PSRAM every time  
- Limited homebrew compatibility  

---

## Required Tools

- EZClient (for patching GBA ROMs and applying SRAM fixes)  
- Cheat Code tools (optional, or manual database edit)  

---

## Recommended Folder Layout

```
/
|-- ezfla_up.bin         # Firmware update file
|-- GBA/                 # Patched GBA ROMs
\-- SAVES/               # SRAM save files (if separated)
```

---

## Firmware & Updates

Firmware updates are typically installed via `ezfla_up.bin` placed on the root of the microSD card.

Latest firmware and tools may still be found via archive mirrors, GBAtemp threads, or preserved EZFlash.cn links.

---

## Notes

- A classic cart with massive community support  
- Great compatibility and still used in retro handhelds today  
- Ideal for users comfortable with manual patching and soft reset workflows  

---

*Contribute fixes or enhancements via [GitHub Issues](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/issues)*
