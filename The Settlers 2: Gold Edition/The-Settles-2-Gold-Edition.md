# The Settlers 2: Gold Edition

This guideline describes how to set up Heroic Games Launcher on Linux to play The Settlers 2: Gold Edition in DOS box available on [GOG.com](https://www.gog.com/en/).
Tested on [Arch Linux](https://archlinux.org/) using [Omarchy](https://omarchy.org/) with [Hyprland](https://hypr.land/).

Version: 1.5.1
GOG store link: <https://www.gog.com/en/game/the_settlers_2_gold_edition>

## MIDI setup

Do these steps if timidity is not installed yet:
1. Install [timidity++](http://archlinux.org/packages/extra/x86_64/timidity++/): `pacman -S timidity++` or from <https://timidity.sourceforge.net/>
2. Start timidity.service: `systemctl --user start timidity.service`
3. Test: `aconnect -o` shall include:
```bash
client 128: 'TiMidity' [type=user,pid=5240]
    0 'TiMidity port 0 '
    1 'TiMidity port 1 '
    2 'TiMidity port 2 '
    3 'TiMidity port 3 '
```

## Proton setup

1. Select Proton version: GE-Proton10-20 (latest at the time of writing this)
2. Keep all settings at default
    * Auto Install/Update DXVK-NVAPI on Prefix: Enabled
    * Enable Esync: Enabled
    * Enable Fsync: Enabled
    * Enable Wine-Wayland: Disabled
    * Enable WoW64: Disabled
    * Enable FRS Hack: Disabled
    * Limet DirectX Games FPS: Disabled
3. Run WINECFG
    * On Graphics tab:
        * Enable a virtual desktop: Enabled
        * Desktop size: 1920x1080
    * On Input tab:
        * Automatically capture the mouse in full-screen windows: Enabled
4. Enable Cloud Save Sync (optional)

## Graphics settings

1. Run Graphic Mode Setup
    * On Basic Settings tab:
        * Select Graphics mode: DDraw
        * Full screen: Enabled
    * On Advanced Settings tab:
      * Keep Aspect Ratio: Enabled
      * Double Buffering: Disabled
      * Scaling Engine: hq2x
      * Window Resolution: original
2. Save Settings
3. Start Game

## Audio settings

1. When the game started, a DOS window will open up.  
Type: 3 (Game DOS Settings)
2. Select: `Setup sound`
3. Select: `Select and configure MIDI music driver`
    * Select: `Roland MT-32 MIDI with MPU-401 MIDE Interface`
    * Use: `Attempt to configure sound driver automatically`  
You should get a message: `Device detected successfully.`
4. Select: `Select and configure digital audio driver`
    * Select: `Creative Labs Sound Blaser 16 or AWE32`
    * Use: `Attempt to configure sound driver automatically`  
You should get a message: `Device detected successfully.`
5. Close setup by selecting: `Done` and then `Quite program`

## Enjoy

After this point the game should be ready to run, with a beautiful MIDI music (I was shocked how good this sounds compared to the windows DOS box version).

## Tested on

* OS: Arch Linux
* Kernel: x86_64 Linux 6.17.1-arch1-1
* Dirtro: Omarchy v3.0.2
* WM: Hyprland 0.51.1
* Heroic Games Launcher: 2.18.1
* Timidity++: 2.15.0-12

