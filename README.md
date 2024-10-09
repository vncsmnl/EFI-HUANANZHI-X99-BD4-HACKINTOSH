# HUANANZHI X99 BD4 + Intel® Xeon® E5-2670 v3 + AMD Radeon™ RX 6600 + Fenvi T919

![Image alt text](/Images/1.png)

<div align="center">
<img src="./Images/2.png">
</div>

[![Apple Badge](https://img.shields.io/badge/Apple-000?logo=apple&logoColor=fff&style=flat)](https://www.apple.com/)
[![macOS Badge](https://img.shields.io/badge/macOS-000?logo=macos&logoColor=fff&style=flat)](https://www.apple.com/macos/ventura/)
[![Intel Badge](https://img.shields.io/badge/Intel-0071C5?logo=intel&logoColor=fff&style=flat)](https://www.intel.com.br/content/www/br/pt/products/sku/81709/intel-xeon-processor-e52670-v3-30m-cache-2-30-ghz/specifications.html)
[![AMD Badge](https://img.shields.io/badge/AMD-ED1C24?logo=amd&logoColor=fff&style=flat)](https://www.amd.com/pt/graphics/amd-radeon-rx-6600-series)
[![Bluetooth Badge](https://img.shields.io/badge/Bluetooth-0082FC?logo=bluetooth&logoColor=fff&style=flat)](https://fenvi.com/product_detail_16.html)

**Latest working macOS**: 15.0.1
<br>
**Current OpenCore**: 1.0.2

---

## Complete hardware specs

- Motherboard Name:	Huananzhi X99-BD4 | Motherboard Chipset:	Intel Lynx Point - B85, Intel Haswell-EP
- CPU Type: 12-Core Intel® Xeon® E5-2670 v3, 2266 MHz (23 x 99)
- Memory: 2 X 16 GB DDR4-3200 Reg. ECC DDR4 SDRAM - Atermiter
- Video Adapter: AMD Radeon™ RX 6600  (8176 MB)
- Audio Adapter: Realtek ALC887 @ Intel Lynx Point PCH - High Definition Audio Controller
- Ethernet Adapter: Realtek PCIe GbE Family Controller
- Network Adapter: Broadcom 802.11ac Network Adapter
- Disk Drive: XrayDisk 1TB SSD  (953 GB)

## What works

- macOS Sequoia, Sonoma, Ventura, Big Sur, Catalina and macOS Monterey
- Audio
- HDMI/DP (in dGPU - Works OOB)
- All USB ports
- Everything iCloud related (Drive, iMessage, Facetime, unlock with Apple Watch, etc)
- Temperature monitoring for everything
- DRM content (Netflix, ATV+, Airplay 2 mirroring etc)
- Shutdown/Reboot/Update to newer macOS builds over time
- Resizable Bar ON (ResizeUsePciRbIo = true)
- Wi-fi/Bluetooth/AirDrop - OpenCore Legacy Patcher

## Kexts used:

- [x] AppleALC.kext
- [x] CpuTscSync.kext
- [x] FeatureUnlock.kext
- [x] Lilu.kext
- [x] RealtekRTL8111.kext
- [x] RestrictEvents.kext
- [x] SMCSuperIO.kext
- [x] SMCProcessor.kext
- [x] USBMap.kext
- [x] VirtualSMC.kext
- [x] WhateverGreen.kext
- [x] XHCI-unsupported.kext

## How does it works (if you have the same hardware): @ThalesM1
  0. Config the BIOS, expecs bellow
  1. Get the EFI
  2. Config the SMBIOS, generating one with genSMBIOS, then edit it using properTree: ROM, SystemUUID, MLB, system serial number
  3. Download **macOs Catalina** from macrecovery
  4. Create the bootable pen drive, install Catalina from Open Core
  5. Update from oficial Apple


## BIOS Settings: @ThalesM1
Access the bios, using DEL key during start
## Disable
  1. Go to advanded -> ACPI settings -> ACPI sleep state -> disable
  2. Go to advanded -> NCT55320 Super IO configuration -> Serial Port 1 -> serial port -> disable
  3. Go to advanded -> CSM Configuration -> video -> change to UEFI -> disable
  4. Reboot the machine
  5. Go to advanded -> CSM Configuration -> CSM Support -> disable
  6. IntelRCSetup -> Processor Configuration -> MSR Lock Control -> disable
  7. IntelRCSetup -> Processor Configuration -> Execute Disable Bit -> disable

 ## Enable
 1. Go to advanded -> USB Configuration -> XHCI Hand-off -> enable
 2. Go to advanded -> USB Configuration -> EHCI Hand-off -> enable
 3. InterRCSetup -> Processor Configuration -> Hyper Threading -> enable


## Benchmark Results:

Geekbench v5            |  Geekbench v6
:-------------------------:|:-------------------------:
[CPU Benchmark](/Benchmark/CPU_Benchmark_v5.png) |  [CPU Benchmark](/Benchmark/CPU_Benchmark_v6.png)
[GPU Metal](/Benchmark/GPU_Benchmark_Metal_v5.png) |  [GPU Metal](/Benchmark/GPU_Benchmark_Metal_v6.png)
[GPU OpenCL](/Benchmark/GPU_Benchmark_OpenCL_v5.png) |  [GPU OpenCL](/Benchmark/GPU_Benchmark_OpenCL_v6.png)

## Thanks/Credits

- [Opencore Team](https://dortania.github.io/getting-started/)
- [BASE-EFI-INTEL-HEDT-4THGEN-X99-HASWELL-E](https://github.com/luchina-gabriel/BASE-EFI-INTEL-HEDT-4THGEN-X99-HASWELL-E)
- [Gabriel Luchina](https://github.com/luchina-gabriel)

## Discord - Universo Hackintosh

- [Access Discord](https://discord.universohackintosh.com.br)

<div><img align="right" src="./Images/vncsmnl.gif" alt="signature" width="200"></div>
<div><img align="left" src="./Images/rate1_w.png" alt="like" width="80"></div>
