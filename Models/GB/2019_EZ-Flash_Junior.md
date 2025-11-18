# EZ-Flash Junior (2019)

[Alternate Repo with some more details](https://github.com/daid/ezflashjr)

The EZ-Flash Junior is a flash cartridge designed for Game Boy and Game Boy Color systems. It delivers modern storage features while retaining compatibility with the original hardware.

---

## Key Features

- Supports Game Boy and Game Boy Color games  
- microSD card support (FAT32, up to 32GB recommended)  
- Real-Time Clock (RTC) built-in  
- Cheat engine (limited support)  
- Firmware and Kernel upgradable via SD  
- Drag-and-drop ROM loading (no patching needed)  
- In-game soft reset (via button combo)  

---

## File Layout

```plaintext
/ (root)
├── EZFLASHJR.BIN         # Kernel file (must be in root for updates)
├── GBC_ROM.gbc
├── GB_ROM.gb
└── SAVE/
    └── GBC_ROM.sav        # Optional: auto-created on save
```

---

## Save Support

- Uses battery-backed SRAM (internal battery required)  
- Auto backs up save files to microSD upon reset or powering off **after returning to the menu**  
- If you power off mid-game or pull the cart without menu return, **your save will not be written** to SD  
- Compatible with 32K SRAM and MBC-based save types  

---

## Known Limitations

- No save states  
- No native support for homebrew with custom save types  
- RTC doesn’t work until it’s set in the settings screen  
- Save loss if user powers off mid-game without returning to menu
- Doesn't sort files alphabetically (See Troubleshooting bellow).

---

## Tools & Firmware

- [EZ Flash Jr Official Firmware & Kernel](https://www.ezflash.cn/download/)  
- Kernel file name: `EZFLASHJR.BIN`  
- Community recommended formatting tool: [guiformat](https://guiformat.com/) (FAT32 only)  

---

## Notes

- Uses a CR2025 battery (user-replaceable)  
- Firmware updates may reset time settings  
- Some original Game Boy games may boot to a black screen unless reset with START+SELECT+A+B  

## Troubleshooting

### EZ-Flash Junior doesn't sort files alphabetically

To sort files alphabetically, you can use the free and open-source project [FATSort (Sourceforge)](https://sourceforge.net/projects/fatsort/). 

```bash
# The device must be unmounted (Linux/Unix)
fatsort /dev/sdXY
```