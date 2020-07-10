TWRP Device Tree for X96 Mini (p212)
===================================

The Amlogic X96 Mini (codenamed _"p212/281"_ or _"ampere"_) have following parameters:

Basic                   | Spec Sheet
-----------------------:|:-------------------------
CPU                     | Octa-core Amlogic S905W
GPU                     | Mali-450 MP
Shipped Android Version | Android 7.1.2
Memory                  | 8 or 16 GB + 1GB or 2GB DDR3 RAM
MicroSD                 | microSD, up to 32 GB (dedicated slot)
Network                 | 10 / 100M Ethernet, WIFI 802.11 b / g / n
Video                   | HDMI 2.0a + HDR, AV 3,5mm.
USB                     | USB 2,0x2
Power Supply            | 5V / 2A
Misc			| IR-port, and microSD Slot

![Amlogic X96 Max](https://imgaz3.staticbg.com/thumb/large/oaupload/banggood/images/2F/68/0e6dfedd-a64f-450c-8fc3-e4db9803b837.jpg "Amlogic X96 Mini")

## Compile

First checkout Minimal TWRP with OmniROM Tree:

```
repo init -u git://github.com/minimal-manifest-twrp/platform_manifest_twrp_omni.git -b twrp-9.0
repo sync
```

And execute these:

```
export ALLOW_MISSING_DEPENDENCIES=true # Only if using Minimal TWRP Tree
. build/envsetup.sh
lunch omni_p212-eng
mka recoveryimage
```

## Installing:

Testing it:
```
fastboot boot out/target/product/onclite/recovery.img
```

Flash it via fastboot:
```
fastboot flash recovery recovery.img
```

Or use Official TWRP App to install it.
