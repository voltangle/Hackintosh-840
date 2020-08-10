![](https://img.shields.io/badge/complete-yes-green)
![](https://img.shields.io/badge/Latest%20supported-Big%20Sur%20Public%20Beta%201-orange)

# Hackintosh 840
This repo contains EFI configuration, kext and many other for HP ElteBook 840 G3 laptop.

## Compatibility table
### If the macOS version is not included in this list, it means that that version is not supported

| macOS Codename | macOS Version | Support | Planned support | Stability |
| --- | --- | --- | --- | --- |
| Big Sur | 11.0 Public Beta 1 | Yes | Yes | N/a(Not tested) |
| Big Sur | 11.0 Developer Beta 3 | Yes | No | N/a(Not tested) |
| Big Sur | 11.0 Developer Beta 2 | No | No | N/a(Not tested) |
| Big Sur | 11.0 Developer Beta 1 | No | No | N/a(Not tested) |
| Catalina | 10.15.6 | Yes | Yes | Stable |
| Catalina | 10.15.5 | Yes | Yes | Stable |
| Catalina | 10.15.2 | Yes | No | Stable |


## Note: Big Sur is not tested. Maybe that installation will be unstable. Big Sur is added to supported versions list because of Clover r5120 update, where in changelog developers said that this release includes kernel patching patterns for Big Sur. If you want to test it out, feel free to try and report result to Issues.

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
