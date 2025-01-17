# macOS on RedmiBook Pro 14 (AMD)
## [OpenCore](https://github.com/acidanthera/OpenCorePkg) 1.0.1
## News
The microphone needs to be downloaded[AMDMicrophone](https://github.com/qhuyduong/AMDMicrophone)For specific use, please check the archive in the warehouse.
## Update
The new EFI has been adapted to the latest system, Sonoma.

The new EFI (Sonoma) are updated with the latest drivers and OpenCore, and this update improves the boot speed, almost seconds.

Remember to replace your three yards.



## Specifications

Type | Spec
:---------|:---------
Model Name      | RedmiBook Pro 14 2021
CPU              | AMD Ryzen™ 7 5700U
RAM           | 16 GB 3200 MHz DDR4
Wi-Fi             | MT7921 replaced with Intel® Wi-Fi 6 AX210
Audio       | Realtek High Definition Audio

## macOS Update History
- ✅ macOS Sonoma 
- ✅ macOS Ventura [old README](EFI/README.md)

## What's working

Type | Status
:---------|:----------
CPU | ✅
AMD GPU Acceleration | ✅
CPU & GPU Power Management | ✅
Audio | ✅
Intel Wi-Fi | ✅
Battery Status | ✅
Shutdown / Reboot |✅
Bluetooth |✅
Sleep |✅
Microphone | ✅
## What's not working

Type | Info | Status
:---------|:---------|:----------
USB | At the moment we need to disable one of the two USB controllers, so the ports connected to it will NOT work even in other OSes, until the setting is reverted in UMAF. | ⚠️
Airdrop | Airdrop is not working.|❌

## Instructions

### Pre-Installation

#### Disabling XHCI1

https://github.com/DavidS95/Smokeless_UMAF

## Notes
Please disable the Secure Boot Mode in BIOS.

Add drivers and do not disrupt the original driver order.

Please use OCAT to modify config.plist, not Propertree.

Please use GenSMBIOS to generate your three codes and change them!!!

NootedRed be disabled initially, and it can only be turned on after the installation is completed.


## Kexts used

Kext | Info
:---------|:---------
[NootedRed](https://github.com/NootInc/NootedRed) | AMD core graphics drivers, the most important.
[AirportItlwm](https://github.com/OpenIntelWireless/itlwm) | Intel Wi-Fi support. Disable for MediaTek Wi-Fi
[AMDRyzenCPUPowerManagement](https://github.com/trulyspinach/SMCAMDProcessor) | AMD CPU Power Management
[AppleALC](https://github.com/acidanthera/AppleALC) | Fixes audio
[AppleMCEReporterDisabler](https://files.amd-osx.com/AppleMCEReporterDisabler.kext.zip) | Disables AppleIntelMCEReporter which causes panics on AMD CPUs
[ECEnabler](https://github.com/1Revenger1/ECEnabler) | Battery reading fixes
[FeatureUnlock](https://github.com/acidanthera/FeatureUnlock) | Fix Continuity Camera on macOS Ventura
[Lilu](https://github.com/acidanthera/Lilu) | Patch Engine
[NVMeFix](https://github.com/acidanthera/NVMeFix) | NVMe Power Management
[RadeonSensor](https://github.com/aluveitie/RadeonSensor) | Temperature readings for AMD GPUs. Disable for NVIDIA GPUs
[RestrictEvents](https://github.com/acidanthera/RestrictEvents) | Change CPU Name
[SMCAMDProcessor](https://github.com/trulyspinach/SMCAMDProcessor) | Companion to AMDRyzenCPUPowerManagement
[SMCBatteryManager](https://github.com/acidanthera/VirtualSMC) | Enables battery reading
[SMCRadeonGPU](https://github.com/aluveitie/RadeonSensor) | Companion to RadeonSensor. Disable for NVIDIA GPUs
[USBToolBox](https://github.com/USBToolBox/kext) | Useful USB ACPI renames and prerequisite for UTBMap
[UTBMap](https://github.com/USBToolBox/tool) | USB Map
[VirtualSMC](https://github.com/acidanthera/VirtualSMC) | Advanced Apple SMC emulator in the kernel
[VoodooPS2Controller](https://github.com/acidanthera/VoodooPS2) | PS/2 Keyboard support
  
## SSDTs Used
  
SSDT | Info
:---------|:---------
[SSDT-PLUG-ALT](/Extras/Decompiled%20ACPI%20Files/SSDT-CPUR.dsl) | Fixes CPU definitions.
[SSDT-EC](/Extras/Decompiled%20ACPI%20Files/SSDT-EC.dsl) | Adds a fake Embedded Controller device.
[SSDT-HPET](/Extras/Decompiled%20ACPI%20Files/SSDT-HPET.dsl) | Fixes IRQ conflicts.
[SSDT-SBUS-MCHC](/Extras/Decompiled%20ACPI%20Files/SSDT-SBUS-MCHC.dsl) | Fixes AppleSMBus.
[SSDT-USBX](/Extras/Decompiled%20ACPI%20Files/SSDT-USBX.dsl) | Enables USB Power Management.
[SSDT-XOSI](/Extras/Decompiled%20ACPI%20Files/SSDT-XOSI.dsl) | Spoof macOS to Windows for some ACPI features.

## Credits

- [qhuyduong](https://github.com/qhuyduong) basic EFI is available.
- [Dortania](https://dortania.github.io) for their awesome guides.
- [Apple](https://www.apple.com) for macOS.
- [Acidanthera](https://github.com/acidanthera) for OpenCore and most Kexts.
- [ExtremeXT](https://github.com/ExtremeXT) for the instruction to disable XHC1

- And anyone else that helped to develop and improve hackintoshing.
