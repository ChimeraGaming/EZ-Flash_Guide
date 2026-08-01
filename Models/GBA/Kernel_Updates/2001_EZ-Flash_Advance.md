# EZ-Flash I / II Software and Loader History

## Identification Note

This page covers the original EZ-Flash I and EZ-Flash II cartridges from the official EZ-FLASH product line.

These cartridges are sometimes incorrectly called the EZ-Flash Advance. They should not be confused with the separate EZF Advance cartridge, which used different hardware, software, drivers, and transfer cables.

The original EZ-Flash I / II cartridges do not use an independently downloadable kernel like the EZ-Flash IV, Omega, or newer models.

Their cartridge menu, game patches, and loader are generated and written by the Windows-based EZClient software.

---

## Current Preserved Software

- Officially listed client: EZClient 3.25
- Community-archived client: EZClient 3.26
- Separately numbered kernel: None
- Separately numbered firmware: None
- Supported products:
  - EZ-Flash I
  - EZ-Flash II
  - EZ-Flash II PowerStar
- Operating system: Legacy 32-bit Windows
- Writer hardware: Compatible EZ-Writer USB hardware

[Official EZ-FLASH Legacy Download](https://www.ezflash.cn/download/)

The official EZ-FLASH download page currently provides EZClient 3.25.

EZClient 3.26 is preserved by community archives, but it is not currently listed on the official EZ-FLASH download page.

---

## Software Version History

| Version | Status | Changes |
| --- | --- | --- |
| 3.26 | Community archived | Later client preserved by the community. A complete official changelog is not currently available. |
| 3.25 | Latest official preserved release | Final version currently distributed through the official EZ-FLASH legacy download page. |
| Earlier 3.x releases | Historical | Added compatibility updates, save patches, loader changes, Nintendo DS support, and newer game definitions over time. Complete changelogs are not preserved. |

Do not assign undocumented fixes to a specific EZClient version unless an original release note is found.

---

## Client and Loader Relationship

EZClient performs several separate functions:

- Communicates with the EZ-Writer
- Detects the cartridge and its capacity
- Formats the cartridge
- Adds or removes games
- Applies save-type patches
- Applies compatibility patches
- Creates the multi-game selection menu
- Writes the loader and game compilation to cartridge NOR
- Imports and exports save data
- Configures optional features supported by the cartridge revision

The loader is included in the cartridge image created by EZClient.

There is no separate kernel file that can be copied to removable storage.

Updating the loader normally requires rewriting the cartridge through EZClient.

---

## Basic Setup

1. Back up every save stored on the cartridge.
2. Install a supported 32-bit version of Windows or prepare a Windows XP virtual machine.
3. Install the EZ-Writer USB driver included with EZClient.
4. Connect the writer directly to a powered USB port.
5. Avoid passive USB hubs.
6. Insert the cartridge into the writer.
7. Start EZClient.
8. Wait for the cartridge and capacity to be detected.
9. Add the desired GBA files.
10. Configure save types or other patches when required.
11. Write the completed compilation to the cartridge.
12. Do not disconnect the writer or remove the cartridge while data is being written.

Formatting or rewriting the cartridge can erase games, loader data, and saves.

---

## Modern Windows Compatibility

EZClient and its drivers were designed for older 32-bit versions of Windows.

Modern 64-bit Windows versions may reject the unsigned legacy USB driver.

The most reliable options are:

- A physical Windows XP computer
- A Windows XP virtual machine with USB passthrough
- A compatible older 32-bit Windows installation

When using a virtual machine:

1. Connect the EZ-Writer to the host computer.
2. Pass the writer through to the Windows XP guest.
3. Install the driver inside the guest.
4. Watch for the USB device to disconnect and reconnect under a different identifier.
5. Pass the device through again if required.

Do not assume that EZClient is frozen while Windows is waiting for the writer to reconnect.

---

## GBA XCODE Compatibility Updates

Later compatibility definitions were sometimes distributed separately from the main client.

A preserved update identified as GBA XCODE `2805`, dated August 28, 2008, was intended for:

- EZ-Flash I
- EZ-Flash II
- EZ-Flash III
- EZ-Flash IV
- EZ-Flash V with 3-in-1

For EZClient, the updated XCODE files were placed in the client's `sysbin` folder and used to replace the older files with the same names.

XCODE updates are game-patching and compatibility data. They are not cartridge firmware.

Translated games, ROM hacks, and heavily modified ROMs may not match the official XCODE database.

---

## Save Management

The original EZ-Flash cartridges use onboard save memory.

EZClient can:

- Read save data from the cartridge
- Write save data to the cartridge
- Associate save data with individual games
- Apply save-type patches
- Back up saves to the computer

Before formatting or rewriting the cartridge:

1. Connect the cartridge to EZClient.
2. Export every important save.
3. Confirm that the backup files were created.
4. Keep a second copy outside the EZClient installation folder.

A weak or failed cartridge battery may cause pending save data or cartridge settings to be lost.

Battery type and replacement procedure depend on the exact cartridge revision.

---

## Loader and Game Compilation

The cartridge menu is rebuilt when games are written through EZClient.

Changing the game list may require rewriting the full cartridge image rather than individually copying files.

The resulting compilation can contain:

- The EZ-Flash loader
- Multiple GBA games
- Save patches
- Compatibility patches
- Game names and menu data
- Optional cheats or trainers
- Nintendo DS-related patches on supported setups

Older cartridges use NOR flash, so writing or erasing a full cartridge can take several minutes.

Do not interrupt the operation.

---

## EZ-Flash II PowerStar

The EZ-Flash II PowerStar is a hardware revision of the EZ-Flash II.

Different writer and driver revisions existed during the product's lifetime.

Possible compatibility symptoms include:

- Cartridge not detected
- Writer not detected
- Client remaining on initialization
- Incorrect capacity shown
- Write operation failing immediately
- Cartridge working with one driver package but not another

Use the complete driver package supplied with the selected EZClient version.

Do not mix individual driver files from several releases unless necessary for troubleshooting.

---

## Known Problems

### Writer Not Detected

Possible causes include:

- Missing USB driver
- Unsupported 64-bit driver environment
- USB passthrough not enabled in a virtual machine
- Writer connected through an incompatible hub
- Damaged USB cable
- Dirty cartridge or writer contacts
- Wrong driver package for the writer revision

Connect the writer directly to the computer and test it inside Windows XP.

### Cartridge Not Detected

- Clean the cartridge contacts
- Reinsert the cartridge firmly
- Restart EZClient
- Reconnect the writer
- Test another USB port
- Test another supported EZClient version
- Confirm that the writer itself is detected by Windows

### Incorrect Cartridge Capacity

Do not format or write the cartridge when EZClient reports the wrong capacity.

This can indicate:

- Incorrect driver
- Failed cartridge detection
- Incompatible writer revision
- Damaged cartridge memory
- Poor cartridge contact

### Failed or Interrupted Write

An interrupted write may leave the cartridge without a usable loader.

Reconnect the cartridge and rewrite the complete compilation.

Do not remove power during:

- Formatting
- Loader writing
- Game writing
- Save restoration

### Games Freeze or Fail to Save

Possible causes include:

- Incorrect save-type patch
- Old XCODE data
- Modified ROM
- Incorrectly trimmed ROM
- Cheat or trainer conflict
- Failing cartridge battery
- Corrupted write
- Hardware failure

Test a verified clean ROM without cheats or additional patches.

### Virtual Machine Reconnection

The writer may disconnect and reconnect during initialization.

Some virtual-machine software treats the reconnected writer as a new USB device.

Pass the device through to the Windows XP guest again before restarting EZClient.

---

## Upgrade Warnings

- There is no standalone kernel update file.
- Do not use `ezfla_up.bin`.
- Do not install EZ-Flash III, IV, Omega, Air, Junior, or Parallel files.
- Export saves before formatting or rewriting the cartridge.
- Do not interrupt a write or erase operation.
- Confirm that the detected cartridge capacity is correct.
- Use the driver included with the selected EZClient package.
- Keep archived copies of working software and drivers.
- Scan third-party archives before running preserved executables.

---

## Notes

- The official legacy download is EZClient 3.25.
- EZClient 3.26 is preserved through community archives.
- The cartridge loader is generated by EZClient.
- No separate kernel version is installed manually.
- Compatibility data can be updated through the client's `sysbin` folder.
- Legacy 32-bit Windows is normally required.
- Keep backups of working drivers, clients, ROM lists, and saves.
- This page covers the original EZ-Flash I / II line, not EZF Advance.

---

## Sources

- [Official EZ-FLASH Download Page](https://www.ezflash.cn/download/)
- [Community EZClient 3.26 Archive](https://gbatemp.net/download/ezclient.3290/)
- [EZ-FLASH Cartridge History](https://gbasp.ru/ezflashhistory1-en.html)
