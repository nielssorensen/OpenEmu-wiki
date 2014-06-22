When pairing for the **very first time**, you need to:
* Use the latest version of OpenEmu (1.0.3) or greater.
* Have Bluetooth enabled on your machine.
* Remove any previous Wiimote pairings stored in Bluetooth prefs.
* Remove third party apps/kexts that cause conflicts (DarwiinRemote, WJoy - these are NOT required!). Unload kexts for WJoy via Terminal.app with the following command: `sudo kextunload -b com.alxn1.driver.wjoy`
* Go to OpenEmu Control prefs and select "Add a Wiimote..." from the bottom menu.
* IMPORTANT: Reset your Wiimote by pressing the red button on the back or inside the battery cover. **If you get a "Pairing Request" dialog popping up asking for a "Passcode" then you have not reset your Wiimote via the red button!**
* Press the "Start Scanning" button from the OE dialog and hold the ①+② buttons on your Wiimote.

Your Wiimote will pair, vibrate and be available in the bottom menu ready for mapping controls or gameplay. **Please note that currently your LED's will NOT be active as it completes pairing.**

When pairing the **next time**:
* Have Bluetooth enabled on your machine.
* Press and hold the ①+② buttons on your Wiimote as you start OpenEmu and your Wiimote will pair and vibrate. Alternatively, return to OpenEmu Control prefs and pair it from the "Add a Wiimote..." menu again.
