Deployment Manual
=================

This manual assumes that you own an Android phone.

Option 1: Install the debug app onto your phone
-----------------------------------------------

### Enable developer options on your phone.

#### Find the version of android your phone is running

1.	Navigate to the settings menu of your phone
2.	Navigate to About Phone
3.	Scroll and find the 'Android version' of your phone

#### Enable developer mode on your version of Android

1.	Go to [google.com](google.com)
2.	Search "How to enable developer option Android [your version number]"
3.	Follow a tutorial to enable developer mode for your android version

### Enable USB debugging

1.	Navigate to the new Developer options menu
2.	Scroll and find the USB debugging option and make sure it is enabled
3.	Scroll and find the 'Verify apps over USB' option and make sure it is enabled

### Installing the app

1.	Plug your phone into your computer via USB
2.	Open Android Studio after completing all the steps in [Development](./Development.md).
3.	At the top menu above the editor, find the device dropdown menu and select your phone.
4.	Click on the 'run' button (shaped like a play button)
5.	Wait for the app to install and load on your phone.
6.	Click the 'stop' button (shaped like a square)

Option 2: Build the APK File
----------------------------

1.	Open Android Studio after completing all the steps in [Development](./Development.md).
2.	Open the terminal view by clicking on the tab at the bottom of the IDE.
3.	In the terminal, type 'flutter build apk' and press enter.
4.	Wait for the command to finish.
5.	The APK can be located at [project-root]/build/app/outputs/apk/app.apk
6.	To install to a device, follow the steps found [here](https://www.cnet.com/how-to/how-to-install-apps-outside-of-google-play/).
