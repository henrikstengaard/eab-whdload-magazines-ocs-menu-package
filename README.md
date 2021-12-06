# EAB WHDLoad Magazines OCS Menu Package

EAB WHDLoad Magazines OCS Menu package contains menus for AGS2 and iGame with screenshots and details for all OCS magazines currently available in Retroplay's WHDLoad packs at English Amiga Board. Menus, screenshots and details are generated using powershell scripts and data files from https://github.com/henrikstengaard/amiga-whdload-game-scripts.

Screenshots and details for all OCS magazines are based on Retroplay's WHDLoad packs downloaded December 4th 2021.

**Note that this package only supports Retroplay's WHDLoad packs at English Amiga Board as paths to start magazines are specifically generated for Retroplay's WHDLoad packs.**

## Features

EAB WHDLoad Magazines OCS Menu package contains following features:

- Arcade Game Selector 2 v2020-04-14, https://github.com/MagerValp/ArcadeGameSelector.
- Arcade Game Selector 2 preconfigured menu with screenshots at resolution 320x128 and 12 colors and magazine details.
- iGame v2.0 2020-10-16, https://github.com/MrZammler/iGame.
- iGame preconfigured menu with screenshots at resolution 320x128/320x256 and 255 colors.

## Requirements

EAB WHDLoad Magazines OCS Menu package can be installed on any Amiga OS and requires about 11MB free space on a harddrive for installation.

For EAB WHDLoad Magazines OCS Menu package to work properly, it requires following applications and libraries are installed:
- MUI: Install MUI from http://aminet.net/util/libs/mui38usr.lha.
- GuigFX MCC for MUI: Install "guigfx.mcc" from http://aminet.net/dev/mui/MCC_Guigfx.lha.
- TextEditor MCC for MUI: Install "TextEditor.mcc" from http://aminet.net/dev/mui/MCC_TextEditor-15.47.lha or http://aminet.net/dev/mui/MCC_TextEditor_68k.lha depending on CPU is 68000 or better.
- Render Library: Install "render.library" from http://aminet.net/dev/misc/renderlib31.lha.
- GuigFX Library: Install "guigfx.library" from http://aminet.net/dev/misc/guigfxlib.lha or http://aminet.net/dev/misc/guigfxlib_nofpu.lha depending FPU is installed.
- WHDLoad: Install WHDLoad from http://whdload.de/whdload/WHDLoad_usr.lha.
- Soft-kicker: Install Soft-kicker from http://aminet.net/util/boot/skick346.lha.
- Kickstart roms for WHDLoad: Use Kickstart roms from Cloanto Amiga Forever or own dumps.

These applications and libraries are already installed, if HstWB or ClassicWB FULL, ADV, ADVSP package is installed using HstWB Installer.

HstWB Installer can automatically identify and install Kickstart roms for WHDLoad. See more details https://github.com/henrikstengaard/hstwb-installer.

For manual installation without HstWB or ClassicWB, use following guides:
- Install MUI: http://guide.abime.net/wb3.1/chap6.htm
- Install iGame, libraries, SKick, WHDLoad and Kickstart roms: http://www.awmosoft.nl/downloads/igame.pdf

## Installation

Download latest release from https://github.com/henrikstengaard/eab-whdload-magazines-ocs-menu-package/releases and copy it to HstWB Installer "packages" directory, which typically is "c:\Program Files (x86)\HstWB Installer\Packages".

Installation through HstWB Installer will install and configure EAB WHDLoad Magazines OCS Menu package using defined assigns.

## Assigns

Installation of EAB WHDLoad Magazines OCS Menu package requires and uses following assigns:

- SYSTEMDIR: = DH0:
- MENUSDIR: = DH1:Menus
- FRONTENDSDIR: = DH1:
- MAGAZINESDIR: = DH1:WHDLoad/Magazines

AGS2 and iGame magazine frontends, AGS2 support files will be installed and configured in SYSTEMDIR: assign. AGS2 menus and WHDLOAD directories will be installed in MAGAZINESDIR: assign.

EAB WHDLoad Magazines AGA Menu package will automatically update SYSTEMDIR:S/Assign-Startup and SYSTEMDIR:S/Startup-Sequence with following assign:

- A-Magazines: = DH1:WHDLoad/Magazines

This assign is required for AGS2 to work as run files use it to start magazines. 

## AGS2

For AGS2 following features had been added in ".Settings" folder:

- Favourites mode: Add or remove magazines in ".Favourites" folder in AGS2 menu.
- Music: Turn music on and off for AGS2 menus.
- WHDLoad ButtonWait: Turn ButtonWait option on or off.
- WHDLoad ExpChip: Turn ExpChip option on or off.
- WHDLoad NoAutoVec: Turn NoAutoVec option on or off.
- WHDLoad NoCache: Turn NoCache option on or off.
- WHDLoad NoVBRMove: Turn NoVBRMove option on or off.
- WHDLoad Preload: Turn Preload option on or off.
- Settings: View and save settings for Favourites mode, Music and WHDLoad options.

Favourites mode can be set to the following:

- Add: Adds magazine to favourites and returns to AGS2 menu
- Add & Run: Add magazine to favourites and run it using WHDLoad.
- Remove: Queues magazine to be removed from favourites and returns to AGS2 menu.
- Off: Default run magazine using WHDLoad.

When turned on music a random .mod file is played while AGS2 menu is shown and will stop before running a magazine. By default there aren't installed any music .mod files. They can be must copied to directory "MENUSDIR:Menu/AGS2Magazines/Music" (unless changed).

WHDLOAD ButtonWait option makes WHDLoad wait for pressing a button when it shows pictures and/or plays music.

WHDLoad ExpChip option forces WHDLOAD to allocate required memory in Chip Memory and may result in performance degration.
This option can be turned on as an attempt to slow down magazines.

WHDLoad NoAutoVec option ensures WHDLoad doesn't quit, if unexpected autovector interrupt or NMI occurs.
This option can be turned on, if WHDLoad crashes with error message "NMI Autovector".

WHDLoad NoCache option makes WHDLOAD disable all caches. 
This option can be turned on as an attempt to slow down magazines.

WHDLoad NoVBRMove option moves the vector table using the VBR (Vector Base Register) to a different memory location.
This option can be turned on as an attempt to fix issues running magazines.

WHDLoad Preload option makes WHDLoad load data files and disk images into memory to increase performance.
This option is turned on by default to avoid screen flickering, when magazines are loading data files.
For lowend Amiga's without Fast memory or accelerator, this option can be turned off, so they can still run most WHDLoad magazines.

To preserve settings between reboots, use "Save settings" to write settings to harddisk.

## Screenshots

Screenshots of EAB WHDLoad Magazines OCS Menu package.

### AGS2 screenshots

Screenshots of browsing magazines in AGS2.

![AGS2 1](screenshots/ags21.png?raw=true)

![AGS2 2](screenshots/ags22.png?raw=true)

Screenshots of settings in AGS2.

![AGS2 3](screenshots/ags23.png?raw=true)

### iGame screenshots

Screenshots of browsing magazines in iGame.

![iGame 1](screenshots/igame1.png?raw=true)

![iGame 2](screenshots/igame2.png?raw=true)

### Workbench screenshots

Screenshots of AGS2 Magazines and iGame installed in System, Magazines drawer for Workbench.

![Workbench 1](screenshots/workbench1.png?raw=true)

![Workbench 2](screenshots/workbench2.png?raw=true)

### WHDLoad magazines screenshot

Screenshot of Directory Opus with left panel at DH1:WHDLoad/Magazines and right panel at PC: (added through WinUAE) ready for copying WHDLoad magazines from PC to WHDLoad magazines drawer.

![dopus_whdload_magazines.png](screenshots/dopus_whdload_magazines.png?raw=true)

### Music for AGS2 screenshot

Screenshot of Directory Opus with left panel at DH1:Menus/AGS2Magazines/Music and right panel at PC: (added through WinUAE) ready for copying mod music files from PC to AGS2 magazines menu.

![dopus_ags2magazines_music.png](screenshots/dopus_ags2magazines_music.png?raw=true)