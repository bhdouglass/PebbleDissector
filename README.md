# PebbleDissector

A Wireshark dissector for the serial protocol used by the Pebble smartwatch

pebble.lua is a small (and not complete!) Wireshark dissector for the serial protocol that is exchanged between the Pebble smartwatch and smartphone.

## Snooping on Pebble communications

NOTE: This setup requires an Android device

* Install [Wireshark](https://www.wireshark.org/)
* Setup the [Pebble Dissector](https://github.com/bhdouglass/PebbleDissector) in Wireshark
    * A guide for adding the dissector: <https://delog.wordpress.com/2010/09/27/create-a-wireshark-dissector-in-lua/>
* Setup [developer options](https://wiki.cyanogenmod.org/w/Doc:_developer_options) on Android
* In the developer options enable "Enable Bluetooth HCI snoop log"
* Do something interesting with your Pebble
* Send the bluetooth log (`/sdcard/btsnoop_hci.log`) to your computer with Wireshark
* Load btsnoop_hci.log into Wireshark
    * If Wireshark does not automatically detect the Pebble portions of the log you will need to use the option "Decode As" and make sure options for "BT RFCOMM" are selected

Original guide found here: <http://wordpress.meulenhoff.org/?p=996>
