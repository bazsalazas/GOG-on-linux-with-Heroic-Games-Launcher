# Pharaoh + Cleopatra Gold Edition

This guideline describes how to set up Heroic Games Launcher on Linux to play Pharaoh + Cleopatra Gold Edition in DOS box available on [GOG.com](https://www.gog.com/en/).  
Tested on [Arch Linux](https://archlinux.org/) using [Omarchy](https://omarchy.org/) with [Hyprland](https://hypr.land/).

* Version: 2.1
* GOG store link: <https://www.gog.com/en/game/pharaoh_cleopatra>

## Proton setup

1. Select Proton version: GE-Proton8-32 (I tried many different versions, this was the one working best for me)
2. Update settings
    * Auto Install/Update DXVK-NVAPI on Prefix: Enabled
    * Enable Esync: Enabled
    * Enable Fsync: Enabled
    * Enable Wine-Wayland: Enabled
    * Enable DDR: Disabled
    * Enable WoW64: Disabled
    * Enable FRS Hack: Disabled
    * Limit DirectX Games FPS: Disabled
3. Run WINECFG
    * On Graphics tab:
        * Enable a virtual desktop: Disabled
    * On Input tab:
        * Automatically capture the mouse in full-screen windows: Enabled
4. Enable Cloud Save Sync (optional)

## Monitor settings

The game takes no matter what the mouse inputs from the top left monitor according to my findings.  
If you want to play on a different monitor, you need to change the monitor settings, e.g. disable the top left monitor (my case).  
You can do this convinently by setting up a shell script to run before game is launched ant after the game exited in the Advanced tab of Heroic Games Launcher.

## Enjoy

After this point the game should be ready to run.

## Tested on

* OS: Arch Linux
* Kernel: x86_64 Linux 6.17.1-arch1-1
* Distro: Omarchy v3.0.2
* WM: Hyprland 0.51.1
* Heroic Games Launcher: 2.18.1
