# Hackintosh EFI for Gen 4 AMD ThinkPad E14

Opencore version 0.9.5

This is a mostly functioning EFI for the ThinkPad E14 gen 4 (AMD version).

DISCLAIMER: This is a work in progress, so I am not responsible for any damage that may occur to your computer. Use at your own risk.
Also, it is generally recommended to build your own EFI, so use only as a last resort or as a guide.

* Resources folder is NOT included in EFI. Download it [here](https://github.com/acidanthera/OcBinaryData/tree/master/Resources) and add it to your OC folder.
* Also, the current config.plist does NOT have a serial number. Download CorpNewt's GenSMBIOS to create one [here](https://github.com/corpnewt/GenSMBIOS).

*** Do NOT include the Tools folder in your EFI folder. ***

## My Specs:

- Ryzen 7 5825U 
- Vega 8 iGPU
- 16GB DDR4-3200 SODIMM RAM (8GB Soldered + 8GB SODIMM)
- NVME SSDs: 
    256GB (Windows) + 512GB (Opencore)
- Intel AX200
- RTL8188 (Ethernet)
- ALC3287/257


## Working:

- iGPU + Hardware Accelration (via NootedRed)
- Ethernet
- Camera
- Keyboard, Trackpad, and Trackpoint
- Audio (Mostly)
- Dual Boot
    
## What doesn't work:

- Airplay, Sidecar, etc.
- Internal Mic
- Sleep (Very inconsistent)

## Works in progress:

- Fixing sleep
- Fixing internal mic

## Installation instructions:

### Steps
1. Download the lastest package
2. Modify Config.plist as needed
3. Set BIOS settings
4. Add to EFI folder of USB installer (EFI/OC & EFI/BOOT)
5. Go through installation process
6. Apply post-install fixes

### Pre-install

- Before installing, you need to create your own SMBIOS via CorpNewt's genSMBIOS. The plist is configued to MacBookPro16,3, so generate serials according or use a different model (NOTE: MBP16,1 and 16,4 expect a dGPU and will cause issues with the iGPU).
- Make sure to (CMD + R) everytime you add any new files to the OC folder.
  

### Post-Install

- Recommended: Set VRAM to 2GB (or 4GB) in BIOS for improved graphics performance
    - If you have 8GB RAM, it is not recommended to upgrade to 4GB
    - This option is under Config/Display in the ThinkPad BIOS
- Recommended: Change CPU name to actual CPU 
- OPTIONAL: Remove Ryzen power management as it can cause some instability




