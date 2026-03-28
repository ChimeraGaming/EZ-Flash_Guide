## EZ-Flash Omega - Crystal Oscillator Replacement Guide

Related discussion: [Issue #3 - Crystal Oscillator Failure (No Nintendo Logo)](https://github.com/ChimeraGaming/GBA-EZ-Flash-2025-Guide/issues/3)

If your EZ-Flash Omega boots **without showing the Nintendo logo**, and you've already:

- Cleaned the cartridge pins  
- Reformatted the SD card to FAT32 (64K allocation)  
- Reloaded the kernel (`ezkernel.bin`)  
- Held `R` during boot to force a kernel reflash  
- Tested in another GBA/SP device  

Then the issue may be a **faulty crystal oscillator**.

---

### Identifying the Faulty Component

The oscillator is a small silver 4-pin SMD part, labeled `24.545`, located just below the yellow RTC battery.

#### Oscillator Location  
![image](https://github.com/user-attachments/assets/6d72e5a4-8943-4c26-8fc9-d30adceea00a)

---

### Replacement Specifications

| Property   | Value                         |
|------------|-------------------------------|
| Type       | Crystal Oscillator (XO or TCXO) |
| Frequency  | 24.545 MHz                    |
| Voltage    | 3.3V                          |
| Output     | CMOS / HCMOS                  |
| Package    | 3225 (3.2 mm x 2.5 mm)        |
| Pads       | 4-pad SMD                     |

---

### Recommended Part Search

Due to limited availability, we recommend manually searching for a compatible oscillator:

- [Digi-Key Oscillator Search](https://www.digikey.com/en/products/filter/oscillators/151)
- [Mouser Oscillator Search](https://www.mouser.com/c/timing-devices/oscillators/)
- [Octopart Cross-Vendor Search](https://octopart.com/search?q=24.545%20mhz%20oscillator%203.3v%203225)

**Search Terms**:  
```
24.545 MHz oscillator 3.3V 3225 SMD
```

Make sure your part exactly matches the specifications above.

---

### Replacement Tips

1. Use hot air or a fine-tip iron to desolder the old oscillator  
2. Clean the pads with flux and solder wick  
3. Align and reflow the new 3225 oscillator carefully  
4. Once installed:
   - Insert your microSD card with a fresh `ezkernel.bin`
   - Hold `R` on boot to reload the kernel
   - Test the cart in a known working GBA/SP

---

### Notes

- Only replace this part if you're confident with SMD soldering or have access to proper tools.
- Ensure the frequency is **exactly 24.545 MHz** - other values will cause the cart to fail detection.
