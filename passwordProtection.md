# BMS Password protection

In my reverse engineering tasks I could not evaluate any option to password protect the BMS, at least the models I'm using (JBD-SP15S001).

It looks like the security was "outsourced" to the bluetooth module. The "old" sets of Xiaoxiang / jiabaida BMS were sold with BLE Module supporting setting the PIN with dedicated AT Commands (and the BMS Bluetooth name too!)

Unfortunately since 2017 the new Bluetooth modules are factory pre-programmed chips with fixed Bluetooth name (Xiaoxiang BMS) and no PIN support.
This is the one I have.

My solution is to implement the password protection on the iOS App level.

**IMPORTANT!!! This solution will prevent ONLY iOS users with the latest App version to access your password protected BMS!!!**

Anyone with Android App or the PC App will be still able to access your BMS!

The solution will provide two PINs (alphanumeric)
- PIN BMS access. If set, you need to provide PIN for reading the data. It is possible to "remember" the PIN so you do not have to re-enter it each time the BMS is connected.
- PIN for BMS configuration. If set, whenever you go to Config screen, you have to provide correct pin.



## Setting PIN

To set the PIN, connect to the BMS and go to Config -> BMS Config. Scroll down to BMS Name / PIN Section. Do not forget to press "Write EEPROM" at the end!



## PIN Reset / Recover
The PIN codes are written in plain text in the BMS name field. So if you do not remember them, you can connect to the BMS with PC App to get them or reset by writing "NONAME" into the name field.

