What done:

create app via: react-native init
npm install --save react-native-ble-plx
npm install
react-native link react-native-ble-plx


this section of android https://github.com/Polidea/react-native-ble-plx#android-example-setup
insall android SDK.
set ANDROID_HOME

in Android device:
make the phone as developer. (tap 7 times on build number in 'settings' => 'about' or something like that).
go to "developers options" and enable USB DEBUGGER .
Go to Settings > Apps and notifications > App permissions > Location Permissions and my app was turned off for some reason. Turning it on resolved the problem.

execute adb command to verify the device is readble in your computer by:
\path\to\Android\Sdk\platform-tools	adb devices

how to execute:
open CMD command eand execute the following 2 commands:
react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res

react-native run-android

