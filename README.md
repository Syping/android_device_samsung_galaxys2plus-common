Common device tree for Samsung Galaxy S II Plus (GT-I9105 and GT-I9105P)
==================================

Note:
-------------
This device requires additional patches to the sources of ROM.
You can find them here: "https://github.com/Syping/android_build-tools/tree/cm-12.1/patches".
If you follow "How to build" instruction the repo "android_build-tools" will be downloaded into "build-tools" folder in the root of ROM's directory.

How to build:
-------------

Initialize repo:

	repo init -u https://github.com/LineageOS/android.git -b cm-12.1
	curl --create-dirs -L -o .repo/local_manifests/manifest_samsung_galaxys2plus-common.xml -O -L https://raw.githubusercontent.com/Syping/android_device_samsung_galaxys2plus-common/cm-12.1/manifest/manifest_samsung_galaxys2plus-common.xml
	repo sync

Compile:

	cd build-tools
	./resync
	./patch
	./build s2plus
