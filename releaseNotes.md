# Release Notes

## v1.2.25
* BMS Settings Screen: from BMS Firmware version 20 you can protect your settings on BMS side. with this version we added option to unlock BMS if settings area is protected with hardware pin.
NOTE: Setting hardware pin and changing bluetooth dongle name is under development and will come with next release!
* BMS Screen: show firmware version

## v1.2.22 - 2020.03.27
Fixed invisible NTC toggles (config section) on older devices (< iOS 13)

## v1.2.20 - 2020.11.20
Increased max cell to 32 (config section)

## v1.2.19 - 2020.10.05
* added support for BMS with HC01 bluetooth dongle
* Notification screen: fixed decimal truncation with locales using comma

## v1.2.17 - 2020.09.02
Fixed connection problem (stuck on "waiting for data") for BMS with empty name.

## v2.0.1 - 2020.08.31 (not yet released in AppStore, only Testflight)
Added recording option into CSV file.
CSV files shared with other iOS Apps (Excel / Number) or downloaded directly on mac.

## v2.0.0 - 2020.xx.xx (not yet released in AppStore)
This is the new v2 Version of XiaoXiang BMS rewritten with SwiftUI. available for iOS(13+), iPad and MacOS (Catalina+)

* multiple BMS Battery View on one screen

## v1.2.16 - 2020.06.09
* BMS Config screen: number of cells is now configurable

## v1.2.15 - 2020.06.06
* Added support for BMS with Bluetooth V5 (2020)

## v1.2.14 - 2020.04.30
* Fix for crash with newer BMS models

## v1.2.13 - 2020.04.14
* BMS Config screen: added support for NTC configuration

## v1.2.12 - 2020.02.16
* BMS Config screen: minimal battery (pack) voltage is now 1V (before 10V)

## v1.2.11 - 2020.01.05
* Cell delta voltage notification shows min/max cell index and voltage
* BMS Screen: show index of min/max cell voltage

## v1.2.10 - 2019.11.17
* Fixed in-App store crash on latest iOS 13 version

## v1.2.9 - 2019.11.14
* Fix DarkMode for PIN Screen
* Fix Chinese translation
* Some bug fixes

## v1.2.8 - 2019.10.30
* iOS13 BugFixes

## v1.2.7 - 2019.10.10
* New language support: Chinese, French, Spanish

## v1.2.6 - 2019.09.18
* build with Xcode11 GM seed 2

## v1.2.5 - 2019.09.15
* build with XCode11 GM seed

## v1.2.4 - 2019.09.13
* Dark mode support

## v1.2.3 - 2019.08.28
* New language support: German
* File Sharing: you can backup your BMS configurations on Desktop PC over iTunes File Sharing
* BMS Screen:
    * Battery Cycle Count is now displayed (number of full discharge/charge cycles)
* BMS List Screen:
    * Show BMS Mac address instead of iOS random generated bluetooth UUID

## v1.2.2 - 2019.08.07
* New language support: Polish
* notification popups disabled when configuring BMS
* UI optimisations

## v1.2.1 - 2019.07.31
* New notification types:
    * BMS lost connection
    * BMS re-connected
    * Cell delta voltage
* Landscape mode on iPhone

## v1.2.0 - 2019.07.20
* Notifications support on iPhone an Apple Watch. It is now possible to define notifications for:
    * Battery SOC
    * Battery Voltage
    * Charging / Discharging
    * Cell Voltage
    * Temperature
* Config Screen: New Tab Notifications

## v1.1.8 - 2019.07.03
* Bug Fix: Voltage Calibration - missing Write button. is now back!
* Bug Fix: Fixed re-purchasing Problem
* Config Screen: Setting for temperature in Celsius or Fahrenheit
* Config screen: extended Designed Capacity and Cycle Capacity fields to 6 digits

## v1.1.7 - 2019.06.18
* Maintenance update. Fix App crash on checksum calculation for specific BMS type.

## v1.1.6 - 2019.06.16
* iPad support. The screen UI is now scaled to iPad

## v1.1.5 - 2019.06.12
* Bug Fix: Demo Device config section available without in-App purchase
* code cleanup

## v1.1.4 - 2019.06.07
* Config screen: extended Current Charge / Discharge field to 6 digits. Label fix.

## v1.1.3 - 2019.06.03
* Support for JBD-SP05S002 BMS
* Config Screen: configuration save / open support added
* Config Screen: new fields for protection configuration
    * Barcode field
    * Cell over temperature trigger, Cell over temperature release, protection delay for charging
    * Cell over temperature trigger, Cell over temperature release, protection delay for discharging
    * Cell under temperature trigger, Cell under temperature release, protection delay for charging
    * Cell under temperature trigger, Cell under temperature release, protection delay for discharging

## v1.1.2 - 2019.05.15
* Config Screen: new fields for protection configuration
    * Cell over voltage trigger, Cell over voltage release, protection delay
    * Cell under voltage trigger, Cell under voltage release, protection delay
    * Pack (Battery) over voltage trigger, Cell over voltage release, protection delay
    * Pack (Battery) under voltage trigger, Cell under voltage release, protection delay
    * Charge over current, release delay, protection delay
    * Discharge over current, release delay, protection delay
* Config Screen: fixed writing Functional Configs: Switch, SCRL, LED_EN and LED_NUM

## v1.1.1 - 2019.01.28
* Config Screen: ability to change the BMS Name (on the hardware, not iOS alias or bluetooth module)
* Config Screen: ability to set PIN1 or PIN2 for protection
* BMS Read protection (PIN1 Code)
* BMS Config protection (PIN2 Code)
* BugFix: fixed crash for BMS without temp sensors

To understand PIN limitations please read: https://github.com/smagicld/xiaoxiangBMS/blob/master/passwordProtection.md


## v1.1.0 - 2018.11.03
* Config Screen: New config screen for cell voltage calibration
* BMS Screen: New section with BMS information like manufacturing date, name and protection counters (how many times protection xyz was activated)
* Connection Screen: Bluetooth devices list sorted by name
* Info Screen: InApp purchases restore
* InApp purchase: writing to BMS is now Pro function. for next 2 months it is for free, so everyone who bought the app before can get this functionality.


## v1.0.11 - 2018.10.15
* WatchOS support: now you can check the most important data on your apple watch
* BMS Screen: max voltage of cell was not visible on smaller screens (iphone5s). fixed.
* BMS Screen: added session logging like max/min voltage, max power (discharge), max charging current and max discharging current
* BMS Screen: fixed disconnection bug when received unknown/not implemented BMS command.
* General: as long the App is connected to BMS, it will stay in background (iOS). This is for future release to do data logging.


## v1.0.10 - 2018.09.16
* Config screen: option to enable/disable balancer
* Config screen: option to enable/disable balancer only while charging
* Config screen: balancer start voltage setting (define when balancer starts balancing)
* Config screen: balancer cell delta voltage setting (balancer tries to balance until delta is below this value)
* Config screen: Functional Configuration swiitches for: Switch, Scrl, Led EN, Led Num. See Xiaoxiang PC software for detailed description
* Config screen: Improved read/write EEPROM. Now, if data packed is not received the read/write will be re-tried for 5 times 
* Config screen: Keyboard hides automatically if tapped outside edit box

## v1.0.9 - 2018.07.06
* Config screen: all capacity parameters now available
* Config screen: progress bar while reading/writing eeprom

## v1.0.8 - 2018.07.01
* Config screen for BMS current (Charge and Discharge) calibration.
* Config screen for BMS capacity settings

## v1.0.7 - 2018.06.12
* Config option to leave charging port on while battery (discharging port) is off
* Coming back from config screen disabled refreshing of the BMS screen. fixed.

## v1.0.6 - 2018.06.08
* Charging and discharging MOSFET On/Off over the app (BMS main screen)

## v1.0.5 - 2018.06.06
* Demo Device switch status is now stored
* Added BMS config screen (BMS Screen -> config button under the output arrow)
* Added BMS name alias feature. Now you can rename the BMS (from "xiaoxiang BMS") as you want

## v1.0.4 - 2018.05.19
* Added support for older Xiaoxiang BMS bluetooth modules (< 2018)

## v1.0.3 - 2018.04.30
* Fixed crash on 32bit iOS devices

## v1.0.2 - 2018.04.27
* Added search spinner on main screen to indicate if the app is searching for devices
* Added status label on main screen to show if bluetooth is disabled or unsupported on the device
* Cosmetic UI changes
* Demo device: extended random data / refresh rate to 20 seconds
* Improved bluetooth re-connection

## v1.0.0 - 2018.04.21
* Initial release for Xiaoxiang BMS and bluetooth module from 2017
