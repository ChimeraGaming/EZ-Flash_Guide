## RTC Retention Issues

### Overview

Some users experience **RTC (Real-Time Clock)** issues when transferring `.sav` files between authentic Pokémon cartridges, the EZ-Flash Omega DE (EZFODE), R4 cards, and emulators like mGBA. Common symptoms include:

- Berries not growing
- Daily events not triggering
- Clock-based events stuck or out of sync

This occurs when the RTC in `.sav` files becomes inaccurate or desynchronized.

---

### Solutions to Keep RTC Accurate

#### 1. Use mGBA to Adjust RTC

- Load your `.sav` and `.gba` file in **mGBA**
- Let the game run for a few seconds to resync the clock
- Save in-game and export the `.sav`
- Move the updated `.sav` to your EZFODE `/SAVER/` folder

Best for syncing real-time events (e.g., berries, tides, clocks)

---

#### 2. Edit Time-Based Events Using PKHeX

- Load the `.sav` file in **PKHeX**
- While it won't adjust RTC directly, you can view and fix time-sensitive data (e.g., mystery gift timers, daycare status)
- Save and export the file

Use this when timers are broken but you need a quick workaround

---

#### 3. Flash ROMs to NOR Mode on EZFODE

- On the EZFODE, press `SELECT` on your Pokémon ROM and choose **Write to NOR Clean**
- This pins the game to NOR memory, increasing RTC stability
- Ensure the `.sav` has the exact same filename as the `.gba`

Recommended for Gen III Pokémon titles

---

#### 4. Avoid Using GB Operator for RTC Transfers

- The Epilogue GB Operator does not maintain RTC data accurately
- Any delay between dumping and writing can cause time drift
- Use it for backups, not active RTC-based saves

Not currently reliable for RTC synchronization

---

#### 5. Replace Cartridge Battery (Original Carts Only)

- Replace the CR2025 or CR1616 battery in real Pokémon cartridges
- Use tools like the R4 RTC fixer or mGBA to reinitialize RTC

Applies only to original hardware, not flashcarts

---

### Summary Table

| Task                          | Tool          | Purpose                          |
|-------------------------------|---------------|----------------------------------|
| Fix/Sync RTC in `.sav`        | mGBA          | Real-time clock synchronization  |
| Edit time-based save data     | PKHeX         | View/fix events and timers       |
| Preserve RTC between boots    | EZFODE NOR    | Persistent save + RTC stability  |
| Avoid inaccurate clock reads  | GB Operator   | Not RTC-safe (beta limitations)  |
| Physical RTC restoration      | Original Cart | Replace battery + reset RTC      |

---

### Best Practices

Always ensure `.gba` and `.sav` filenames match exactly, and keep them in simple, shallow folders:

```
/GBA/YourGame.gba  
/SAVER/YourGame.sav
```

This improves RTC handling and save detection on flashcarts.
