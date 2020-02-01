Deployment Manual
=================

This manual assumes that you own an Android phone.

Enable developer options on your phone.
---------------------------------------

#### Find the version of android your phone is running

1.	Navigate to the settings menu of your phone
2.	Navigate to About Phone
3.	Scroll and find the 'Android version' of your phone

#### Enable developer mode on your version of Android

1.	Go to [google.com](google.com)
2.	Search "How to enable developer option Android [your version number]"
3.	Follow a tutorial to enable developer mode for your android version

#### Enable USB debugging

1.	Navigate to the new Developer options menu
2.	Scroll and find the USB debugging option and make sure it is enabled
3.	Scroll and find the 'Verify apps over USB' option and make sure it is enabled

Install the app onto your phone
-------------------------------

1.	Plug your phone into your computer via USB
2.	Open Android Studio
3.	At the top menu above the editor, find the device dropdown menu and select your phone.
4.	Click on the 'run' button (shaped like a play button)
5.	Wait for the app to install and load on your phone.
6.	Click the 'stop' button (shaped like a square)

The IDE will build the installation file and install it to your phone. To give the app to others, the installation file is also available at [projectroot]/build/app/outputs/apk/app.apk.

This file can be placed onto any matching Android phone and installed.
