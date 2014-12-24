Philz_touch 汉化版

Fork于Philz-cwm6

<<<<<<< HEAD
中文字库来自xiaolu，在此感谢


使用中文字库办法：

BoardConfig.mk定义

BOARD_USE_CUSTOM_RECOVERY_FONT := \"fontcn46_28x73.h\"

将SD卡链接在data/media/0

RECOVERY_USE_MIGRATED_STORAGE := true
=======
__Home page__
http://forum.xda-developers.com/showthread.php?t=2201860

#### Building

If you haven't build recovery ever before, please look up the thread linked above.
If you regularly build ROMs/Recoveries for your device, and have a working CWM setup
on your build machine, then you can quickly set up and build Philz Touch recovery as well

Check these three patches are present in your build/ directory
   1. https://github.com/CyanogenMod/android_build/commit/c1b0bb6
   2. https://github.com/CyanogenMod/android_build/commit/6b21727
   3. https://github.com/CyanogenMod/android_build/commit/fddc5f4

Clone philz recovery to bootable/recovery-philz folder

    git clone https://github.com/PhilZ-cwm6/philz_touch_cwm6 bootable/recovery-philz -b cm-11.0

Now build with RECOVERY_VARIANT flag set to philz:

    . build/envsetup.sh && lunch && mka -j3 recoveryimage RECOVERY_VARIANT=philz

or

    export RECOVERY_VARIANT=philz
    . build/envsetup.sh && lunch && mka -j3 recoveryimage

or

    add to device BoardConfig.mk:
        RECOVERY_VARIANT := philz
    and run:
        build/envsetup.sh && lunch && mka -j3 recoveryimage
>>>>>>> philz_touch_cwm6_fdb/cm-11.0
