![](https://img.shields.io/badge/complete-yes-green)
![](https://img.shields.io/badge/Latest%20supported-Catalina%2010.15.6-purple)

# Hackintosh 840
This repo contains EFI configuration, kext and many other for HP ElteBook 840 G3 laptop.

## Compatibility table

| macOS Codename | macOS Version | Support | Planned support | Stability |
| --- | --- | --- | --- | --- |
| Big Sur | 11.0 | No | Yes | N/a |
| Catalina | 10.15.6 | Yes | Yes | Stable |
| Catalina | 10.15.5 | Yes | Yes | Stable |
| Catalina | 10.15.4 | Yes | Yes | N/a |
| Catalina | 10.15.3 | No | No | N/a |
| Catalina | 10.15.2 | Yes | No | Stable |
| Catalina | 10.15.1 | No | No | N/a |
| Mojave | 10.14.6 | No | No | N/a |

## Versions
| Version | Revision | Changelog |
| --- | --- | --- |
| 1.3 | Stable | <ul> <li> Added boot chime </li> </ul> |
| 1.2 | Stable | <ul> <li> Tried to add startup chime </li> <li> Fixed issues with backlight </li> <li> Added HiDPI folder for crispier look. </li> </ul> |
| 1.1 | Stable | <ul> <li> Added new Clover Bootloader theme </li> <li> Fixed Clover Bootloader GUI glitch because of missing theme </li> </ul> |
| 1.0 | Stable | <ul> <li> Added support for macOS 10.15.6 </li> <li> Fixed issue with system can't update because of forced boot on Macintosh HD. Boot is still graphical </li> <li> Fixed sound now working </li> <li> Fixed microphone not working </li> </ul> |

## Working components

| Component | Component model | State |
| --- | --- | --- |
| Wifi | Intel Wireless AC 8260 | With bugs |
| Bluetooth | Intel Wireless AC 8260 | Working |
| Graphics | Intel HD Graphics 520 | Working |
| Sound | Bang&Olufsen | Working|
| Battery | N\A(Stock) | Working |
| Trackpad | Synaptics | With bugs |

## Known bugs

 - Apple TV/TV+ doesn't work
 - Wi-Fi doesn't work correct
 - Gestures on trackpad doesn't work
 - The "Charger connected" sound plays only in headphones
 
 If you want to contribute, feel free to create issues and pull requests!
 
 ## Installation
 ### Step one: create bootable USB of macOS
 
 You need a flash drive with size of 16 GB. Then make a bootable USB of macOS on another Mac machine. Borrow a real Mac, or use a Hackintosh.
 
 ### Step two: install Hackintosh
 
 Then, you need to install macOS on your EliteBook 840 G3. Just run macOS Installation, clear drive with Disk Utility, and install macOS using Install macOS option.
 
 
### Step three: postinstall

Download the postinstall .zip package from [Releases](https://github.com/GGorAA/Hackintosh-840/releases) page. Then, launch Kext Utility, and drag&drop `AppleIntelWifiV2.kext` to Kext Utility window. Wait until it finishes the process (it can ask you for your permission with administrator password prompt, just type in your password and go on), and proceed to next step.

### Step four: enjoy!

Now you can enjoy your fresh installation of macOS!
