# eGPU-Setup
This repo is just a place for me to save all the resources I used to build a eGPU for two different MacBookPros, fully functional in both macOS and Windows.
I will not provide instructrions/steps as most of this is striped together from different egpu.io threads public for everyone. I encourage you to visit the following threads for details:
1. [AST-Link-R43SG Setup](https://egpu.io/forums/thunderbolt-enclosures/adt-link-r43sg-tb3/)
2. [DSDT Override Instructions](https://egpu.io/forums/pc-setup/fix-dsdt-override-to-correct-error-12/#post-716)
3. [MacBookPro 16' apple_set_os.efi](https://egpu.io/forums/bootcamp/macbook-pro-16-windows-egpu-error-12-fix/)

### Hardware used:
1. MacBookPro 13' Late 2016 w/ TouchBar
2. MacBookPro 16' 2019
3. AMD Shappire Nitro+ RX 580 8GB
4. ADT-Link R43SG-TU adaptor (basically a PCIe3.0 to M.2 NVMe)
5. Wavlink Thunderbolt 3 NVME External SSD enclosure (40Gbit/s)
6. Thermaltake 850W 80 Plus PSU
7. A homemade aluminium case to fit everything

### Software used:
1. Bootcamp and Bootcamp drivers
2. [Adrenalin April 2020](bootcampdrivers.com) drivers
3. Customized DSDT (dsdt-modified.dsl file in this repo)
4. [automate-eGPU for MBP 13'](https://github.com/goalque/automate-eGPU) as a bootloader.
This will load both, a customized apple_set_os.efi and our dsdt.aml files.
5. [automate-eGPU for MBP 16'](https://github.com/aa15032261/apple_set_os-loader) as a bootloader.
Only apple_set_os.efi is used in this case.
6. Windows 10 Dev Channel 20150.1 Version (or newer?)

### Notes:
* There is no need to compile a new DSDT for MBP 16', they don't need that extra QWordMemory. Just use Clover to open the EFI partition and install automate-eGPU for MBP 16'.
* Disable T2 security on MBP 16'.

### Main issues found:
1. Error 12 (fixed)
2. Lots of Windows BSOD :)
