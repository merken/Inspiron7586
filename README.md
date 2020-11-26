# Dell Inspiron 7586 2 in 1 convertable laptop
OpenCore configuration for the Dell Inspiron 7586 2 in 1

OpenCore version is 0.6.3

Started from scratch using Dortania's Guide https://dortania.github.io/OpenCore-Install-Guide/

PlatformInfo was generated using Dortania's Guide https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake.html#platforminfo
**This is missing in the config.plist** Please generate your own.

Details of the target machine:
- Dell Inspiron 7586 2 in 1
- BIOS 1.7.1
- 8th Generation Intel(R) Core(TM) i7-8565U Processor (8MB Cache, up to 4.6 GHz)
- Intel UHD 620 (device id 0x3EA0, BIOS Device name _SB_.PCI0.GFX0
- Intel Wireless 9560
- NVIDIA GeForce MX150 2GB GDDR5 (not needed or either supported in macOS, will be disabled) BIOS Device name _SB__.PCI0.RP05.PEGP
- 512GB M.2 PCIe NVMe Solid State Drive
- 15.6-inch UHD (3840 x 2160) 4K Touch Screen
- Fingerprint sensor (not supported)
- Originally had 16GBx1, DDR4, 2666MHz, **replaced with 2x Crucial 16 GB SODIMM DDR4-2400**

**CFG LOCK** disabled using Dortania's guide : https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#disabling-cfg-lock
BIOS 1.7.1 and 1.8.0 should all have the same entry for the CFG Lock **0x5C3**
Extracted from 

https://www.dell.com/support/home/en-us/drivers/driversdetails?driverid=9vv9w&oscode=wt64a&productcode=inspiron-15-7586-2-in-1-laptop
and 

https://www.dell.com/support/home/en-us/drivers/driversdetails?driverid=wr5v6&oscode=wt64a&productcode=inspiron-15-7586-2-in-1-laptop

CFL LOCK is disabled by running the modGRUBShell.efi from the OpenCore menu and entering:

```setup_var 0x5C3 0x00```

This needs to be repeated after a new BIOS flash!

CFL LOCK can be re-enabled by running the modGRUBShell.efi from the OpenCore menu and entering:

```setup_var 0x5C3 0x01```

## Tips
Please follow the Dortania Guide carefully
Please use PropertTree for any modifications to your config.plist!

## Special thanks
Hacker1024 (superl2) for his initial work:
https://github.com/hacker1024/Dell-Inspiron-7586-Hackintosh
