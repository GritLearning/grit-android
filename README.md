grit android cordova wrapper
============================

This is the Android wrapper for the `grit` project. To get things set up you need to do the following:

Android SDK setup
-----------------
Download the SDK from http://developer.android.com/sdk/index.html or `brew install android-sdk` if you are on a Mac and use homebrew.
Then bring up the Android SDK Manager (or run `android` on the console) and install at least: 
- SDK Tools
- Platform Tools
- Build Tools
- Androind 4.3 or whatever is currently the target

This should set you up with a working Android development environment. You may also want to grab the debug keystore from
Dropbox to build binaries that can replace our official debug builds on tablets.

Repository setup
----------------

clone the `grit-android` repository next to the main `grit` repository. Open up a console and link `grit` 
into the `assets` folder like this:

    $ ln -s ../grit assets/www
    
This will link the main grit app into the cordova wrapper. After this compile the build by running:

    $ ant debug

This should generate a `bin/Grit-debug.apk` that can be copied to the device. If you have the tablet connected via USB
you can run the following command to copy the binary over:

    $ adb install -r bin/Grit-debug.apk
    
If you into trouble shout out on the mailing list and then enhance the docs here with what you learned.
