<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/TOTEM_logo_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/TOTEM_logo_bright.svg">
  <img alt="TOTEM logo font" src="/docs/images/TOTEM_logo_bright.svg">
</picture>

<h1 align="center">T O T E M - S H I F T</h1>

# ZMK CONFIG FOR THE TOTEM-SHIFT SPLIT KEYBOARD

[Here](https://github.com/Endracion/TOTEM-SHIFT) you can find my updated TOTEM-SHIFT hardware files.\
[Here](https://github.com/GEIGEIGEIST/totem) you can find the original hardware files and build guide.

TOTEM-SHIFT is a modified 38 keys column-staggered split keyboard originally by GEIGEIGEIST running [ZMK](https://zmk.dev/). It's meant to be used with a SEEED XIAO BLE.

It includes these additional projects and features:
- caksoylar's [RGB LED Widget](https://github.com/caksoylar/zmk-rgbled-widget)
- carrefinho's [Prospector Dongle](https://github.com/carrefinho/prospector)
- Support for [ZMK Studio](https://zmk.studio/) for keyboard layout adjustment without flashing

![TOTEM layout](/docs/images/TOTEM_layout.svg)

## Nice!Nano IO connect list:

| nice_nano_v2.overlay | Display | 
| :------------------- | :------ |
| SPIM_SCK | SCL |
| SPIM_MOSI | SDA |
| cmd-data-gpios | DC |
| reset-gpios | RES |

## HOW TO USE

- fork this repo
- `git clone` your repo, to create a local copy on your PC (you can use the [command line](https://www.atlassian.com/git/tutorials) or [github desktop](https://desktop.github.com/))
- adjust the totem.keymap file (find all the keycodes on [the zmk docs pages](https://zmk.dev/docs/codes/))
- `git push` your repo to your fork
- on the GitHub page of your fork navigate to "Actions"
- scroll down and unzip the `firmware.zip` archive that contains the latest firmware
- connect the left half of the TOTEM to your PC, press reset twice
- the keyboard should now appear as a mass storage device
- drag'n'drop the `totem_left-seeeduino_xiao_ble-zmk.uf2` file from the archive onto the storage device
- repeat this process with the right half and the `totem_right-seeeduino_xiao_ble-zmk.uf2` file.