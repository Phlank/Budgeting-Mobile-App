Development manual
==================

This manual assumes you are using Windows 10. It's not 100% necessary to use it for your own development environment, but it is the one we used.

Download and install [Git for Windows](https://git-scm.com/download/win)
------------------------------------------------------------------------

-	Run the downloaded file

#### Git for Windows Setup

1.	Click 'Next'
2.	Leave things as they are and click 'Next'
3.	Click 'Next'
4.	Ensure 'Git from the command line and also from 3rd-party software' is selected and click 'Next'
5.	Ensure 'Use the OpenSSL library' is selected and click 'Next'
6.	Ensure 'Checkout Windows-style, commit Unix-style line endings' is selected and click 'Next'
7.	Ensure 'Use MinTTY' is selected and click 'Next'
8.	Ensure 'Enable file-system caching' and 'Enable Git Credential Manager' are selected and click 'Next'
9.	Let it do its thing
10.	Uncheck 'View release notes' and click 'Next'

Download and install the [Flutter SDK](https://flutter.dev/docs/get-started/install)
------------------------------------------------------------------------------------

-	Follow the directions on the website above

Download and install [Android Studios](https://developer.android.com/studio)
----------------------------------------------------------------------------

-	Click on 'Download Android Studios'
-	Agree to the terms and conditions
-	Click on 'Download Android Studios' at the bottom left side of the window
-	Open the downloaded file and select 'Run'

#### Pages of the installer

1.	Select 'Next'
2.	Make sure 'Android Virtual Device' is checked off and click 'Next'
3.	Choose a directory to install to and select 'Next'
4.	Select 'Install'
5.	Let the installer do its thing until you are able to click 'Next'
6.	Ensure 'Start Android Studio' is checked and click 'Finish'

Setting up Android Studios
--------------------------

-	If a dialog asking for importing old configurations appears, select 'Do not import settings' and click 'OK'

#### The setup wizard

1.	In the setup wizard's first screen, click 'Next'
2.	Ensure the radio button 'Standard' is selected and click 'Next'
3.	Pick the Darcula theme and click 'Next'
4.	Click 'Finish'
5.	Let the setup wizard download all the components needed and then click 'Finish'

Starting up Android Studio for the first time
---------------------------------------------

1.	Click on 'Check out project from version control'
2.	Click on 'Git' in the menu that appears
3.	In the new window, type 'https://github.com/Phlank/AccutechBudgetingApp' into the URL text box and click 'Clone'
4.	On the next dialog box, click 'Yes'

#### Inside the editor

1.	Minimize the assistant on the right side
2.	At the bottom right, in the 'Plugins Suggestion' popup, click the downward arrow
3.	In the same popup, click on 'Configure plugins...'
4.	In the new popup, ensure 'Flutter' is selected and click 'OK'
5.	On the new popup, click 'Accept'
6.	A new popup saying Dart needs to be installed will appear. Click 'Yes' on this popup
7.	The popup on the bottom right will appear recommending that you restart Android Studios. Click on 'Restart' here
8.	At the top of the editor is a bar that says 'Dart SDK is not configured'. CLick on 'Download Dart SDK' and follow the instructions on the Dart website to install the Dart SDK
9.	Return to Android Studios and click 'Open Dart settings' in the same bar
10.	In the new dialog, check 'Enable Dart support'
11.	In the Dart SDK path menu, select the path to where you installed the Dart SDK in step 8
12.	Under the text 'Enable Dart support for the following modules:', check 'Project "AccutechBudgetingApp"' and 'AccutechBudgetingApp'
13.	Click 'Apply'
14.	Click 'OK'
15.	Select 'File' -> 'Settings'
16.	In the dialog shown, expand 'Languages & Frameworks' and click on 'Flutter'
17.	Similar to step 11, retrieve the Flutter SDK path
18.	Click 'Apply' and 'OK' in that order
19.	In the bar over the text editor, click 'Get dependencies'

Adding a Google Maps API Key
----------------------------

1.	Get a Google Maps API Key by following the steps found [here](https://developers.google.com/maps/documentation/javascript/get-api-key). Restrict the key using the steps later in the page to mobile apps.
2.	Copy your Google Maps API Key to the clipboard.
3.	In [project-root]/android/local.properties, type 'google.map.key=[PASTE_API_KEY]'
4.	In [project-root]/lib/model, create a new file called 'keys.dart'
5.	In keys.dart, type "const googleMapsAPIKey = '[PASTE_API_KEY]';"

These specific files are not linked with git, so your API key will not be exposed in the repository.

You're done!
------------
