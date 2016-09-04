Android Open Pwn Project
========================

## Getting Started

Please refer to the [Downloading and Building Requirements](https://source.android.com/source/requirements.html) before proceeding.

Install additional dependencies:

    sudo apt-get install schedtool bc

For HTC M8, install lz4:

	git clone https://github.com/Cyan4973/lz4.git
	cd lz4/
	make
	sudo make install

Ensure that OpenJDK 7 is configured as the default Java version:

    sudo update-alternatives --config java
    sudo update-alternatives --config javac

Read the CyanogenMod wiki entry: [Extract proprietary blobs](https://wiki.cyanogenmod.org/w/Build_for_m8#Extract_proprietary_blobs).  Your rom will not boot if the proprietary blobs are not properly extracted before starting the build process.

## Downloading the Source

Please refer to [Downloading the Source](https://source.android.com/source/downloading.html) before proceeding.

To initialize a local repository using this source tree, use the command:

    repo init -u git@github.com:aagallag/android_platform.git -b px-0.1

Then to sync the repository, use:

    repo sync

## Building

Please refer to [Building the System](https://source.android.com/source/building.html) before proceeding.

To initialize the build environment after the repo sync, use the command:

    . build/envsetup.sh

Then to choose a build target, use:

    brunch

Or to specify a target, use:

    brunch <device>
