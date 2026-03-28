# Frequently Asked Questions (FAQ)

This FAQ addresses common questions and concerns about the EZ-Flash Omega Definitive Edition and related tools.

---

### General Usage

**Q: Do I need to patch games before putting them on the EZ-Flash?**  
**A:** No, only if you're playing a ROM hack. Clean games work without patching.

**Q: Why does my ROM not appear on the EZ-Flash menu?**  
**A:** It may be in the wrong folder, corrupted, or unsupported. Check file extension (`.gba`, `.gb`, `.gbc`, `.nes`) and ensure it's not nested too deep.

**Q: Is it safe to remove the SD card while the device is on?**  
**A:** No. Always power off before removing the SD card to avoid save corruption.

---

### Saving Issues

**Q: My save file keeps disappearing. What's wrong?**  
**A:** You may not be saving properly. Always:
1. Save in-game twice  
2. Wait ~5-10 seconds after saving  
3. Return to kernel menu before powering off

**Q: Do I need to press a button to save manually?**  
**A:** No - saves are committed automatically if you return to the kernel menu (unless you turned off autosave). For extra safety, soft reset (`L+R+Select`) to return instead of powering off (if you loaded with Addon).

---

### Themes & Skins

**Q: Can I use any theme on Omega DE?**  
**A:** Only `.skn` themes designed for the Omega DE will work properly. Some Omega (classic) themes may partially work but are untested.

Some themes may also require a custom kernel to be installed to appear correctly. For examples, see [Theme Files.md](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Docs/Theme_Files.md).

**Q: Why is my theme not loading correctly?**  
**A:** Check:
- Your folder is in `/THEMES/`
- The `.skn` file and assets are not nested in subfolders
- Your kernel is updated to the latest version

---

### Thumbnails

**Q: My thumbnails don't appear. What's wrong?**  
**A:** Check the following:
- File is `.bps`
- Name matches exactly the 4-letter ROM serial (use GBATA or RHEA to check)
- Correct folder path: `/IMGS/B/P/BPRE.bmp` (case-sensitive)

**Q: How do I find the correct 4-letter serial?**  
**A:** Use tools like [GBATA](https://www.romhacking.net/utilities/601/) or [RHEA](https://www.romhacking.net/utilities/542/).

---

### Cheats

**Q: Cheats aren't working. Help!**  
**A:**
- Enable cheats from `Start / Options / Cheat Support = On`
- Place `CHEAT.DB` inside `/CHEAT/`
- ROM name must match the entry in the cheat database
- Use converted codes if raw GameShark/CodeBreaker don't work

---

### Files & Folders

**Q: What's the recommended folder structure?**  
**A:**
```
/GBA/
/GB/
/GBC/
/NES/
/THEMES/
/IMGS/
/CHEAT/
```

**Q: Can I use exFAT or NTFS?**  
**A:** Only FAT32 is officially supported. Use 64K allocation size for best results. exFAT may work but can cause issues.

---

### Still Need Help?

Check out:
- [Troubleshooting Guide](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Troubleshooting/README.md)
- [Creating Thumbnails](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Tutorials/Creating_Thumbnails.md)
- [Creating Themes](https://github.com/ChimeraGaming/EZ-Flash_Guide/blob/main/Tutorials/Creating_Themes.md)

Or [submit an issue on GitHub](https://github.com/ChimeraGaming/EZ-Flash_Guide/issues).
