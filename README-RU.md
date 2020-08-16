![](https://img.shields.io/badge/Working-yes-green)
![](https://img.shields.io/badge/Latest%20supported-Big%20Sur%20Public%20Beta%201-orange)
![](https://img.shields.io/github/issues-raw/GGorAA/Hackintosh-840?color=yellow)
![](https://img.shields.io/github/issues-pr/GGorAA/Hackintosh-840)

# Hackintosh 840

В этом репозитории находяться настройки для хакинтоша на HP EliteBook 840 G3. Возможно этот EFI совместим с другими ноутбуками из линейки EliteBook 840(не протестировано)

Сейчас работают над привнесением Bluetooth для беспроводных карт Intel.

## Содержание

  - [Таблица совместимости](#compatibility-table)
  - [Рабочие компоненты](#working-components)
  - [Известные баги](#known-bugs)
  - [Установка](#installation)
    - [Шаг первый: создайте установщик macOS](#step-one-create-bootable-usb-of-macos)
    - [Шаг второй: установите Hackintosh](#step-two-install-hackintosh)
    - [Шаг третий: постинсталл](#step-three-postinstall)
      - [Шаг три.один: исправьте цвета дисплея](#step-threeone-fix-display-colors)
      - [Шаг три.два: установите серийный номер и UUID для исправления работы Apple ID, iCloud, App Store, iMessage и так далее](#step-threetwo-install-serial-number-and-uuid-to-fix-apple-id-icloud-app-store-imessage-and-more)
      - [Шаг три.три: make boot look nice](#step-threethree-make-boot-look-nice)
    - [Шаг четыре: готово!](#step-four-enjoy)

## Compatibility table

### If the macOS version is not included in this list, it means that that version is not supported

| macOS Codename | macOS Version      | Support | Planned support | Stability |
| -------------- | ------------------ | ------- | --------------- | --------- |
| Big Sur        | 11.0 Public Beta 1 | Yes     | Yes             | Stable    |
| Catalina       | 10.15.6            | Yes     | Yes             | Stable    |
| Catalina       | 10.15.5            | Yes     | No              | Stable    |


## Working components

| Component | Component model        | State                 |
| --------- | ---------------------- | --------------------- |
| Wifi      | Intel Wireless AC 8260 | With bugs             |
| Bluetooth | Intel Wireless AC 8260 | Working               |
| Graphics  | Intel HD Graphics 520  | Working               |
| Sound     | Bang&Olufsen           | Working               |
| Battery   | N\A(Stock)             | Working               |
| Trackpad  | Synaptics              | Working(gestures too) |

## Known bugs

 - Apple TV/TV+ doesn't work
 - Wi-Fi doesn't work correct
 - The "Charger connected" sound plays only in headphones
 - iMessage is half-working
 - Location services doesn't work

 If you want to contribute, feel free to create issues and pull requests!

 ## Installation

 ### Step one: create bootable USB of macOS

 You need a flash drive with size of 16 GB. Then make a bootable USB of macOS on another Mac machine. Borrow a real Mac, or use a Hackintosh.

 ### Step two: install Hackintosh

 Then, you need to install macOS on your EliteBook 840 G3. Just run macOS Installation, clear drive with Disk Utility, and install macOS using Install macOS option.


### Step three: postinstall

Download the Postinstall.zip package from release that you are downloading. Now, drag both HeliPort and Hackintool apps to `Applications` folder, open `Applications` folder, right-click on HeliPort, and click `Open`, then click `Open` in dialog. This will prevent macOS from saying `This is a not trusted app`. Next, open System Settings. Click Users & Groups. Select your user, and click `Login items`. Click the `+` icon, and select HeliPort from popup window.

### Step three.one: fix display colors

Go to Apple > System Preferences > Display > Color, then select P3(display). This fixes blue color represented like purple color.

### Step three.two: install serial number and UUID to fix Apple ID, iCloud, App Store, iMessage and more

First, open Hackintool from Launchpad or Spotlight. Go to `System` tab, and in that tab, click `Serial Generator`. At the bottom, select `MacBookPro13,1`, and click at the refresh icon. Now, mount your EFI. Go to `Disks` tab, right-click the EFI partition, and click `Mount`. Then, right-click again, and click `Open`.

Next, navigate to `EFI > OC` and open  `config.plist` in Xcode. Now, expand `Plaforminfo`, and in it `Generic`. In row `SystemProductName` write `MacBookPro13,1`, in row `SystemSerialNumber` paste the Serial Number from Hackintool. The same applies to `SystemUUID`: paste there SmUUID from Hackintool.

### Step three.three: make boot look nice

If you haven't closed your `config.plist` in Xcode, good. If not, open it again. In the menu bar select `Find`, and then `Find in Workspace` or press Shift+Command+F. Now, type in search box `-v`, and click first result. (If nothing appears, proceed to next step.) Then, scroll a little bit down to reveal the selected result. Now, select the text box and delect `-v` part from it (if you're curious what does it do, basically it replaces normal graphical boot with console-like boot. Typically used when debugging).

Restart your Hackintosh to apply all changes made now.

### Step four: enjoy!

Now you can enjoy your fresh installation of macOS!