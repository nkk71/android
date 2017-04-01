
Getting Started
---------------

To get started with TWRP & MULTI-ROM, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

To initialize your local repository using the MULTI-ROM trees, use a command like this:

    repo init -u git://github.com/multirom-dev/android.git -b <branch>

Then to sync up:

    repo sync

Then to build MR TWRP, multirom zip & uninstaller for your device:

     export TARGET_DEVICE=<device_name>
     ./mr-build.sh
     
Or the old-fashioned way:
     
     . build/envsetup.sh; lunch <device_name>-eng

The following is from: https://github.com/Tasssadar/multirom/wiki/Porting-MultiROM

make recoveryimage # builds the recovery image

make multirom # builds multirom binary

make trampoline # builds trampoline - MultiROM's init daemon

make multirom_zip # builds multirom and trampoline and installation ZIP file

make multirom_uninstaller # builds uninstaller ZIP
