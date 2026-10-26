# andr36oid hotfixes

Small fixes you can drop onto an andr36oid card without reflashing it.

Each hotfix is built for one specific release and checks that before doing anything, so on
any other build it quietly does nothing and can't hurt the card. The release each one works
with is listed next to it below. They're all for the **2026-10-24** release right now.

## Hotfixes

### 2026-10-24 release
- **Saving to the games card** - [vold-easyroms-write.fix.zip](https://github.com/andr36oid/hotfixes/raw/main/vold-easyroms-write.fix.zip)
  Lets apps save to the SD card again (save states, and emulators that write next to their files). Fixes saving being blocked on the default storage setting.

- **Soy Sauce speaker** - [soysauce-speaker.fix.zip](https://github.com/andr36oid/hotfixes/raw/main/soysauce-speaker.fix.zip)
  For Soy Sauce V04 clones whose built-in speaker went silent. Sound comes out of the speaker again; plugging in headphones still mutes it.

- **Stop screen pinning** - [no-screen-pinning.fix.zip](https://github.com/andr36oid/hotfixes/raw/main/no-screen-pinning.fix.zip)
  Stops a stray button press from pinning you to one app and leaving you stuck there.

- **USB keyboard & mouse** - [usb-kbm-preset.fix.zip](https://github.com/andr36oid/hotfixes/raw/main/usb-kbm-preset.fix.zip)
  Adds a USB mode that makes the console act as a keyboard and mouse for another device.

- **USB debugging (adb)** - [andr36oid-usb-debug.fix.zip](https://github.com/andr36oid/hotfixes/raw/main/andr36oid-usb-debug.fix.zip)
  Debugging only, for developers. Keeps the console in USB device mode with adb and USB debugging turned on across restarts, so a computer stays connected over the OTG port without re-picking Settings > USB mode each time.
  Warning: while this is installed the OTG port is a USB device for a computer. Do not charge the console while it is active: charging is not allowed in USB device mode (the DC port is the only charge port and must not be used in this mode). Do not plug a powered USB or OTG accessory (controller, stick, keyboard, drive) into the OTG port either. Delete the ZIP from the `hotfix` folder to go back to normal USB mode switching.

## How to apply

Easy way: The SD flasher can apply hotfixes to existing and new cards.

The manual way:

1. Put the card in your computer and open the **BOOT** (or EASYROMS) drive. BOOT is recommended.
2. Make a folder on it called `hotfix`.
3. Copy the `.fix.zip` into that `hotfix` folder. Do not rename or extract the ZIP file.
4. Put the card back and turn the console on.

It reapplies itself on every boot. To undo one, delete its `.fix.zip` from the folder and reboot.

