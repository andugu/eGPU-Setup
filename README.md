# eGPU-Setup
In this write-up I will aim to explain all the steps needed to build a custom eGPU for a MacBookPro, fully functional in both macOS and Windows.
Most of this is striped together from different egpu.io threads.

### Hardware used:
1. MacBookPro 13' Late 2016 w/ TouchBar
2. AMD Shappire Nitro+ RX 580 8GB
3. ADT-Link R43SG-TU adaptor (basically a PCIe3.0 to M.2 NVMe)
4. Wavlink Thunderbolt 3 NVME External SSD enclosure (40Gbit/s)
5. Thermaltake 850W 80 Plus PSU
6. A homemade aluminium case to fit everything

### Software used:
1. Bootcamp and Bootcamp drivers
2. [Adrenalin April 2020](bootcampdrivers.com) drivers
3. Customized DSDT
4. [automate-eGPU](https://github.com/goalque/automate-eGPU) as a bootloader
this will load both, a customized apple_set_os.efi and our dsdt.aml files.
5. Windows 10 Dev Channel 20150.1 Version

### Main issues found:
1. Error 12 (fixed)
2. Lots of Windows BSOD :)
3. 
