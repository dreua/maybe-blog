# Documentation of my experience with LineageOS / MicroG on a Pixel 3a

## Data

* The Pixel 3a by Google is currently available for ~ 160 € refurbished. (2022-05-26)
* The hardware is still good enough for my needs, I like the size of this phone and the fact that it still has a headphone jack.
* Hardware codename: sargo
* Android version: 12 (SP2A.220505.002) by Google. Support by Google will end in May 2022!
* My laptop runs Fedora Linux 35 and some well aged Android Studio and its Android Tools.

## Installation

Starting with a fresh and empty phone, I followed the [guide for LineageOS](https://wiki.lineageos.org/devices/sargo/install) ([PDF Archive](Install LineageOS on sargo - LineageOS Wiki.pdf)):

* First it needed some Android upgrades to get to the version mentioned above. The LineageOS guide recommends "Android 12.1.0". I couldn't confirm that this is actually 12.1 but let's assume it's good enough.

* Fastboot needs root (sudo), you may need to use the full path to fastboot depending on how and where it is installed.
* Installing and running the recovery image worked fine.

* I ended up not installing LineagOS but heading over to MicroG's LineagOS fork at this point. (i.e. Lineage recovery image but still running stock Android. You may want to start with MicroG's recovery image, not sure whether it makes a difference.)

Switching to the [guide called LineageOS for MicroG](https://lineage.microg.org/) ([PDF Archive](LineageOS for microG.pdf)).

* When verifying make sure you use the correct key, there are two in the repository and I ended up tab-completing the wrong one.
* Installing `lineage-19.1-20220526-microG-sargo.zip` according to lineage guide.
* Accept warning about wrong signature.
* Reboot.


Follow the LineageOS for MicroG Post-Install

## Installation Wizard

Looks great

* Set Time and Date (Couldn't find Berlin but Brussles works, too)
* Connect to Wifi via QR Code
* Set to Gesture Navigation. (Google's installer annoyingly does not ask this.)
* Asks for Backup to restore (DavX5, Nextcloud, Flashdrive, on Phone) but I don't have one. Those options sound interesting, though.

## Issues

### DB Navigator: `ERR_UNKNOWN_URL_SCHEME`

Solution: Disable "Browser" (Chromium). Then Firefox / Fennec will automatically used as WebView for the Login screen and it handles the URL scheme just fine.


