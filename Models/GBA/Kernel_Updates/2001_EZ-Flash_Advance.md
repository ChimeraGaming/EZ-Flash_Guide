# EZ-Flash I / II Software and Loader History

## Identification Note

This page covers the original EZ-Flash I and EZ-Flash II cartridges from the official EZ-FLASH product line.

The repository filename uses `EZ-Flash_Advance`, but these cartridges should not be confused with the separate EZF Advance cartridge. EZF Advance used different hardware, transfer software, drivers, and writer equipment.

The EZ-Flash I and II do not use a standalone kernel file like the EZ-Flash IV, Omega, or newer models.

Their cartridge menu, game patches, and loader are generated and written through the Windows-based EZClient software.

---

## Current Preserved Software

- Latest official download: EZClient 3.25
- Latest known release: EZClient 3.26
- Standalone kernel: None
- Separately numbered firmware: None
- Supported products:
  - EZ-Flash I
  - EZ-Flash II
  - EZ-Flash II PowerStar
- Operating system: Legacy Windows
- Writer hardware: Compatible EZ-Writer USB hardware

[Official EZ-FLASH Legacy Download](https://www.ezflash.cn/download/)

[Community EZClient 3.26 Archive](https://gbatemp.net/download/ezclient.3290/)

The official EZ-FLASH download page currently provides EZClient 3.25.

EZClient 3.26 is the newest confirmed release, but it is currently preserved through community archives rather than the official download page.

---

## Confirmed Software Version History

Only versions supported by an official download, preserved changelog, archived software package, or dated contemporary report are included.

| Version | First Confirmed Period | Status | Confirmed Information |
| --- | --- | --- | --- |
| 1.07 | November 2002 | Historical | Confirmed in contemporary EZ-Flash user reports. A complete changelog has not been preserved. |
| 2.06 | February 2004 | Historical | Confirmed official client release. A community-translated Spanish edition and Linker Driver 1.3 were also distributed. |
| 3.00 | February 2004 | Historical | First confirmed 3.x release. Introduced a different writer-driver package from 2.06. |
| 3.01 | March 2004 | Historical | Confirmed through contemporary driver and compatibility discussions. |
| 3.08 | August 2004 | Historical | Improved cartridge recognition, USB-device compatibility, loader cartridge support, soft-reset and cheat handling, and updated XCODE and ROM-name data to 1627. |
| 3.09 | August 2004 | Historical | Fixed an HTTP read error involving the new EZ-FLASH web server and corrected the green/red cartridge-detection indicator behavior. |
| 3.10 | Confirmed by 2006 | Historical | Confirmed installed release. No reliable standalone changelog has been located. |
| 3.11 | Confirmed by 2005 | Historical | Confirmed release and once distributed as the current EZClient version. No complete changelog has been preserved. |
| 3.12 | April 2005 | Historical | Confirmed release used with EZ-Flash II hardware. No complete changelog has been preserved. |
| 3.17 | August 2005 | Historical | Confirmed release. No complete changelog has been preserved. |
| 3.19 | October 2005 | Historical | Confirmed release immediately preceding the Nintendo DS-focused 3.20 branch. |
| 3.20 Beta | Late 2005 | Historical beta | Leaked before the completed 3.20 release. Introduced early Nintendo DS loading functions. |
| 3.20 Final | November 11, 2005 | Historical | Added full Nintendo DS support and allowed FlashMe systems to boot compatible DS software without a PassMe. |
| 3.21 | December 2005 | Historical | Confirmed release following 3.20. No complete changelog has been preserved. |
| 3.22 | Late 2005 to early 2006 | Historical | Confirmed EZ-Flash I and II client release. No complete changelog has been preserved. |
| 3.23 | January 2006 | Historical | Confirmed release. No complete changelog has been preserved. |
| 3.24 | February 2006 | Historical | Confirmed release. No complete changelog has been preserved. |
| 3.25 | April 2006 | Current official archive | Latest version currently distributed through the official EZ-FLASH legacy download page. |
| 3.26 | Confirmed by mid-2006 | Latest known release | Updated Nintendo DS compatibility, turned off the lower DS screen while playing GBA games in DS mode, and updated Goldfinger data for newer GBA games. |

### Version Gaps

The following version ranges may contain additional releases, but they are not listed because sufficiently reliable evidence has not been located:

- Versions before 1.07
- Versions between 1.07 and 2.06
- Versions between 2.06 and 3.00
- Versions 3.02 through 3.07
- Versions 3.13 through 3.16
- Version 3.18

A missing number does not prove that the version was never released.

Do not assign undocumented changes to a particular version unless an original package, official release note, or reliable contemporary record is found.

---

## Major Documented Updates

### EZClient 1.07

EZClient 1.07 is the earliest version currently confirmed in contemporary user reports.

At this stage, EZClient already supported:

- Writing multiple games to an EZ-Flash cartridge
- Managing cartridge save data
- Deleting games from the end of the cartridge list
- Writing complete cartridge compilations
- Communicating with the original EZ-Writer hardware

A complete official changelog has not been preserved.

---

### EZClient 2.06

EZClient 2.06 was a mature release from the 2.x generation.

Confirmed preserved components include:

- EZClient 2.06
- EZ-Flash Linker Driver 1.3
- Community-translated language builds

Contemporary reports indicate that some original EZ-Flash cartridges worked more reliably with EZClient 2.06 than with the first 3.x releases.

EZClient 2.06 and the 3.x series use different driver packages. Do not assume that their writer drivers are interchangeable.

---

### EZClient 3.00 and 3.01

EZClient 3.00 began the 3.x client series in early 2004.

Users upgrading from 2.06 were required to replace or update the writer drivers included with the older client.

Reported symptoms of using the wrong driver included:

- Cartridge appearing and disappearing repeatedly
- Writer indicator flashing between green and red
- Cartridge not being detected
- Client recognizing the cartridge for only a few seconds
- Write functions failing to begin

EZClient 3.01 followed shortly afterward and used the newer 3.x driver family.

Complete official changelogs for 3.00 and 3.01 have not been preserved.

---

### EZClient 3.08

EZClient 3.08 included the following documented changes:

- Fixed Bomberman-type soft-reset problems
- Fixed cheat-support problems when installed in a folder containing spaces
- Added flashing support when a non-EZ cartridge was detected
- Improved cartridge recognition
- Updated XCODE data to version 1627
- Updated ROM-name data to version 1627
- Improved loader cartridge support
- Improved compatibility with USB devices

A corrupted EZ-Loader file was reportedly included with some copies of 3.08. Affected cartridges could display corrupted text instead of the normal EZ-Loader name.

EZClient 3.09 or replacement files from another working client package corrected the problem.

---

### EZClient 3.09

EZClient 3.09 was released one day after 3.08.

Documented changes:

- Fixed an HTTP read error involving the updated EZ-FLASH web server
- Fixed incorrect green and red writer-light behavior when detecting a cartridge

Because of the corrupted loader reported in some 3.08 packages, 3.09 is the preferred preserved release between those two versions.

---

### EZClient 3.10 Through 3.19

The following releases are confirmed, but their full official changelogs have not been preserved:

- 3.10
- 3.11
- 3.12
- 3.17
- 3.19

These releases occurred during a period of frequent updates involving:

- GBA compatibility data
- Save patches
- Loader revisions
- Cheat and Goldfinger data
- Writer recognition
- Nintendo DS preparation
- New game definitions

Specific changes should not be assigned to an individual release without additional evidence.

---

### EZClient 3.20 Beta

A beta version of EZClient 3.20 appeared before the completed release.

This beta introduced early support for changing the cartridge from its GBA loader to a Nintendo DS loader.

The beta was leaked before the official release and should not be treated as the recommended final version.

Possible beta limitations included:

- Incomplete Nintendo DS compatibility
- Unfinished loader behavior
- Save problems
- Missing game patches
- Dependence on particular PassMe or FlashMe configurations

---

### EZClient 3.20 Final

EZClient 3.20 Final was released on November 11, 2005.

Its primary documented addition was full Nintendo DS support for compatible EZ-Flash I and II setups.

Features included:

- Nintendo DS ROM patching
- Nintendo DS loader generation
- FlashMe boot support
- Ability to boot compatible Nintendo DS software without a PassMe when FlashMe was installed
- Continued GBA cartridge management

Nintendo DS operation still depended on:

- Original Nintendo DS or Nintendo DS Lite hardware
- FlashMe, PassMe, EZPass, or a compatible boot method
- Compatible game and save patches
- Correct loader configuration
- Supported cartridge capacity

Nintendo DS compatibility remained less complete than normal GBA compatibility.

---

### EZClient 3.21 Through 3.25

The following later releases are confirmed:

- 3.21
- 3.22
- 3.23
- 3.24
- 3.25

Complete official changelogs have not been preserved for each release.

These builds continued the later EZClient branch after Nintendo DS support was introduced.

EZClient 3.25 remains the version currently provided through the official EZ-FLASH website.

---

### EZClient 3.26

EZClient 3.26 is the latest confirmed EZClient release.

Documented changes include:

- Updated Nintendo DS compatibility for newer games
- Turned off the Nintendo DS lower screen while playing GBA games in DS mode
- Updated Goldfinger cheat data for newer GBA releases

Community notes also recommend processing some Nintendo DS files through EZ4Client before loading them through EZClient when additional compatibility is needed.

EZClient 3.26 is community archived and is not currently offered on the official EZ-FLASH download page.

---

## Client and Loader Relationship

EZClient performs several related functions:

- Communicates with the EZ-Writer
- Detects the cartridge and its capacity
- Formats cartridge memory
- Adds and removes games
- Applies save-type patches
- Applies compatibility patches
- Applies cheat or Goldfinger data
- Generates the multi-game selection menu
- Creates the GBA loader
- Creates the Nintendo DS loader on supported versions
- Writes the completed loader and game compilation to cartridge memory
- Imports and exports saves

The loader is included in the cartridge image created by EZClient.

There is no separate kernel file that can be copied to the cartridge.

Updating the loader normally requires rewriting the cartridge through EZClient.

---

## Driver Compatibility

EZClient packages include drivers for compatible EZ-Writer hardware.

Driver compatibility is important because different client generations may use different drivers.

### Confirmed Driver Change

EZClient 2.06 and EZClient 3.00 or newer use different driver packages.

When moving between major versions:

1. Disconnect the writer.
2. Remove the currently installed legacy driver.
3. Restart Windows when required.
4. Install the driver included with the selected EZClient package.
5. Reconnect the writer.
6. Confirm that Windows detects it correctly.
7. Start EZClient only after driver installation is complete.

Do not freely combine driver files from different EZClient releases.

A mismatched driver can cause:

- Repeated writer disconnection
- Cartridge detection failures
- Incorrect capacity reporting
- Flashing indicator lights
- Time-out errors
- Failed erase operations
- Failed write operations

---

## Basic Setup

1. Back up every important save from the cartridge.
2. Install a supported legacy Windows environment.
3. Install the EZ-Writer driver included with the selected EZClient release.
4. Restart Windows if requested.
5. Connect the EZ-Writer directly to a powered USB port.
6. Avoid passive USB hubs.
7. Insert the cartridge into the writer.
8. Start EZClient.
9. Wait for the cartridge and its capacity to be detected.
10. Confirm that the displayed cartridge capacity is correct.
11. Add the desired GBA files.
12. Configure save types, cheats, or compatibility options when required.
13. Write the completed compilation.
14. Do not remove the cartridge or disconnect the writer during the operation.

Formatting or rewriting the cartridge can erase:

- Games
- Loader data
- Save data
- Cheat data
- Cartridge settings

---

## Modern Windows Compatibility

EZClient and its USB drivers were designed for legacy versions of Windows.

The most reliable environment is:

- Windows XP 32-bit
- A physical older Windows computer
- A Windows XP 32-bit virtual machine with USB passthrough

Modern 64-bit Windows versions may reject the unsigned legacy USB driver.

### Virtual Machine Setup

1. Install a Windows XP 32-bit virtual machine.
2. Enable USB passthrough.
3. Connect the EZ-Writer to the host computer.
4. Attach the writer to the virtual machine.
5. Install the matching EZClient driver inside Windows XP.
6. Watch for the writer to disconnect and reconnect.
7. Pass the reconnected USB device back into the virtual machine if necessary.
8. Start EZClient after Windows detects the writer.

Some writer operations cause the USB device to reconnect using a different device identifier.

The client may appear to freeze while Windows waits for the reconnected writer.

---

## GBA XCODE Compatibility Updates

Later GBA compatibility definitions were distributed separately from the main EZClient program.

A preserved update identified as:

```text
GBA XCODE 2805
2008-08-28
```

was intended for:

- EZ-Flash I
- EZ-Flash II
- EZ-Flash III
- EZ-Flash IV
- EZ-Flash V with 3-in-1

### Installing XCODE Data

1. Close EZClient.
2. Back up the existing `sysbin` folder.
3. Download and extract the XCODE package.
4. Copy the updated files into the EZClient `sysbin` folder.
5. Replace the older files with the same names.
6. Restart EZClient.
7. Rewrite affected games when necessary.

XCODE files contain game-patching and compatibility information.

They are not:

- Cartridge firmware
- A new loader version
- A new EZClient version
- A standalone kernel

Translated games, ROM hacks, and heavily modified ROMs may not match the official XCODE database.

---

## Save Management

The original EZ-Flash cartridges use onboard save memory.

EZClient can:

- Read save data from the cartridge
- Export save data to the computer
- Import save data
- Write save data back to the cartridge
- Associate saves with individual games
- Apply save-type patches
- Adjust save allocation when supported

Before formatting or rewriting the cartridge:

1. Connect the cartridge through EZClient.
2. Export every important save.
3. Confirm that the files were created successfully.
4. Keep a second backup outside the EZClient installation directory.
5. Confirm that each backup belongs to the correct game.

A weak or failed cartridge battery may cause pending save data or cartridge settings to be lost.

Battery type and replacement procedure depend on the exact cartridge model and hardware revision.

---

## Loader and Game Compilation

EZClient creates a complete cartridge compilation containing:

- EZ-Flash loader
- Game-selection menu
- GBA games
- Save patches
- Compatibility patches
- Game titles and menu information
- Optional cheats or trainers
- Nintendo DS loader data on supported versions

Changing the game list may require rewriting some or all of the cartridge image.

Because the cartridges use NOR flash, writing or erasing a full cartridge can take several minutes.

Do not interrupt:

- Formatting
- Erasing
- Loader writing
- Game writing
- Save restoration
- Nintendo DS loader installation

An interrupted operation can leave the cartridge without a working loader.

---

## EZ-Flash II PowerStar

The EZ-Flash II PowerStar is a hardware revision of the EZ-Flash II family.

It remains compatible with EZClient but may require the correct combination of:

- EZClient release
- Writer driver
- EZ-Writer revision
- Cartridge driver mode
- USB controller

Possible compatibility symptoms include:

- Cartridge not detected
- Writer not detected
- Client remaining on initialization
- Incorrect capacity shown
- Write operation immediately failing
- Cartridge working with one client version but not another
- Indicator repeatedly switching between green and red

Use the complete driver package supplied with the selected EZClient version.

Do not mix individual driver files from several releases unless performing controlled troubleshooting.

---

## Nintendo DS Support

EZClient 3.20 and newer include Nintendo DS-related functions.

Nintendo DS operation may require:

- Original Nintendo DS or Nintendo DS Lite
- FlashMe
- PassMe
- EZPass
- Compatible loader settings
- Compatible Nintendo DS ROM
- Correct save patch
- Supported cartridge capacity

The EZ-Flash I and II are GBA-slot cartridges. They are not Slot-1 Nintendo DS flashcarts.

Nintendo DS compatibility is incomplete and should be considered a secondary historical feature.

Possible Nintendo DS limitations include:

- Games larger than the cartridge capacity
- Unsupported save types
- Download Play problems
- Nintendo Wi-Fi compatibility problems
- Anti-piracy protection
- Games requiring later patch databases
- Sleep-mode incompatibility
- PassMe 2 compatibility requirements
- Failure to boot on unmodified systems

Normal GBA operation should be tested separately when diagnosing Nintendo DS problems.

---

## Known Problems

### Writer Not Detected

Possible causes include:

- Missing USB driver
- Wrong driver for the installed client
- Unsupported 64-bit Windows environment
- USB passthrough not enabled
- Writer connected through an incompatible hub
- Damaged USB cable
- Failed writer hardware
- Insufficient USB power

Connect the writer directly to the computer and test it under Windows XP 32-bit.

---

### Cartridge Not Detected

- Clean the cartridge contacts
- Reinsert the cartridge firmly
- Restart EZClient
- Reconnect the writer
- Test another USB port
- Install the driver included with the selected EZClient version
- Test another confirmed EZClient release
- Confirm that Windows detects the writer

---

### Green and Red Indicator Flashing

Repeated green and red flashing can indicate:

- Driver mismatch
- Unstable cartridge detection
- Poor cartridge contact
- Incorrect writer driver
- Damaged cartridge memory
- Incompatible client version

EZClient 3.09 corrected one documented indicator-light problem from the 3.08 release.

---

### Incorrect Cartridge Capacity

Do not format or write the cartridge when EZClient reports the wrong capacity.

Incorrect capacity can indicate:

- Driver communication failure
- Wrong writer driver
- Poor cartridge contact
- Unsupported writer revision
- Damaged cartridge memory
- Incorrectly detected cartridge type

Reconnect the writer and verify the hardware before continuing.

---

### Time-Out Error

A time-out while deleting, erasing, or writing can be caused by:

- Driver mismatch
- USB communication failure
- Writer power problem
- Incompatible USB controller
- Cartridge memory failure
- Damaged writer hardware
- Using a USB hub

Test another direct USB port and reinstall the matching writer driver.

---

### Failed or Interrupted Write

An interrupted write may leave the cartridge without a usable loader.

To recover:

1. Reconnect the cartridge.
2. Confirm that the correct capacity is detected.
3. Back up accessible saves.
4. Format the cartridge when required.
5. Rewrite the complete loader and game compilation.
6. Allow the operation to finish without interruption.

Do not remove power during recovery.

---

### Games Freeze or Fail to Save

Possible causes include:

- Incorrect save-type patch
- Old XCODE data
- Modified ROM
- Incorrectly trimmed ROM
- Cheat or trainer conflict
- Failed write
- Weak cartridge battery
- Unsupported game
- Damaged cartridge memory

Test a verified clean ROM without cheats or additional patches.

---

### Loader Displays Corrupted Text

Some EZClient 3.08 packages reportedly contained a corrupted loader.

Symptoms can include:

- Corrupted characters
- Repeated `ÿ` symbols
- Missing EZ-Loader name
- Menu failing to start normally

Install EZClient 3.09 or replace the affected files in `sysbin` using a known-good package.

---

### Virtual Machine Reconnection

The writer may disconnect and reconnect during initialization.

Some virtual-machine programs treat the reconnected writer as a new USB device.

Attach the device to the Windows XP guest again before restarting EZClient.

---

## Upgrade and Usage Warnings

- There is no standalone kernel update file.
- Do not use `ezfla_up.bin`.
- Do not install EZ-Flash III, IV, Omega, Air, Junior, Parallel, or other model files.
- Export saves before formatting or rewriting the cartridge.
- Do not interrupt a write or erase operation.
- Confirm that the detected cartridge capacity is correct.
- Use the driver supplied with the selected EZClient version.
- Do not mix EZClient 2.x and 3.x drivers.
- Keep archived copies of known-working software and drivers.
- Use the official 3.25 release when testing unexplained problems.
- Use 3.26 when its later Nintendo DS and Goldfinger updates are needed.
- Scan third-party archives before running preserved executables.

---

## Notes

- EZClient 1.07 is the earliest currently confirmed release.
- EZClient 2.06 is a confirmed mature 2.x release.
- EZClient 3.00 introduced a new driver generation.
- EZClient 3.08 and 3.09 have preserved official changelogs.
- EZClient 3.20 introduced full Nintendo DS support.
- EZClient 3.25 remains the official legacy download.
- EZClient 3.26 is the latest known release.
- The cartridge loader is generated by EZClient.
- No standalone kernel is installed manually.
- Compatibility data can be updated through the `sysbin` folder.
- Legacy Windows is normally required.
- Keep backups of working clients, drivers, game lists, and saves.

---

## Sources

- [Official EZ-FLASH Download Page](https://www.ezflash.cn/download/)
- [EZClient 3.26 Community Archive](https://gbatemp.net/download/ezclient.3290/)
- [EZClient 3.26 Preserved Changelog](https://www.dekazeta.net/foro/files/file/848-ezclient/)
- [EZClient 2.06, 3.00, and 3.01 Discussion](https://www.elotrolado.net/hilo_donde-encontrar-ez-client-software-verssion-v2-06_272747)
- [EZClient 3.08 and 3.09 Changelog](https://tweakers.net/downloads/7149/ezclient-309.html)
- [EZClient 3.20 Release Report](https://www.dcemu.co.uk/list/section/1-DCEmu-Featured-News-Articles?page=9841)
- [EZ-Flash Hardware and Software History](https://gbasp.ru/ezflashhistory2-en.html)
- [EZ-Flash I Setup and Software Guide](https://gbasp.ru/ezflash1-en.html)
- [GBA XCODE 2805 Information](https://bbs.newwise.com/thread-232523-1-1.html)
- [EZClient 3.23 Contemporary Report](https://gbadev.net/forum-archive/thread/20/7802.html)
- [EZClient 3.24 Contemporary Report](https://gueux-forum.net/index.php?%2Fprofile%2F31045-kakaman%2Fcontent%2F=&change_section=1)
