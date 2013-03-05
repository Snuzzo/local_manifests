Vigor_Tree
==========

Device Tree for HTC Rezound needed for building AOSP

To initialize your local repository using the Vigor Device trees, use a command like this:

    repo init -u git://github.com/TheBr0ken/Vigor_Tree.git

Then to sync up:

    repo sync

If your building for anything other than CM you must run this command:

    rm device/htc/vigor/overlay/packages/apps/Torch/res/values/config.xml

Building with Linaro requires you to change 2 lines in build/envsetup.sh

Go into your "build" directory:

    cd build

edit envsetup.sh and under:

    ANDROID_EABI_TOOLCHAIN

change:

    arm) toolchaindir=arm/arm-linux-androideabi-4.6/bin

to:

    arm) toolchaindir=linaro/bin
    
also under:

    ARM_EABI_TOOLCHAIN ARM_EABI_TOOLCHAIN_PATH
    
change:

    toolchaindir=arm/arm-eabi-4.6/bin

to:

    toolchaindir=linaro/bin
    
Build AOSP as normal


    
