### ADBDroid.json

## This is a custom driver for NEEO to allow ADB over Meta.
It can be installed as a regular driver by putting ADBDroid.json in the active folder of meta 
(see https://github.com/jac459/meta).

It uses one (1) module that is not delivered within meta from JAC459, namely PythonManager.py.
See https://github.com/Ton-O/NEEO-Meta-Plus for information on its functions and how to install.

## How to use
This driver is used as a custom driver running under the umbrella of meta.
It uses the PythonManager.py module that acs as an interface between ths driver and the actual ADB-code.
PythonManager is content agnostic, meaning it is only used as a communication method, it is totally unaware of the codes that flow through it.  

Some requirements exist for this to function:
- installation specific, see https://github.com/Ton-O/NEEO-Meta-Plus
- Devcice to be controlled via ADB should listen for ADB-connections on the default port 5555. If not, you can change this port in ADBDroid.json.
- Though not required for all devices, it is best to have a personalised adb_key to comply to a more strict security policy of your Android device. See line 44 and on of https://raw.githubusercontent.com/Ton-O/NEEO-Meta-Plus/master/README.MD on how to generate such key.


This custom driver has a number of built-in functions that allow everyone to control any ADB-device with it.
If you're missing an ADB-command, you can quite easily add that to the custom driver, using this list of ADB-commands:
http://developer.android.com/reference/android/view/KeyEvent.html
