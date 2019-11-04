# Dell missing firmware
This repository is for filing issues with firmware updates missing at [LVFS](https://fwupd.org) for [Dell](https://www.dell.com) systems.

When filing a request please include the following items:
* A link to the firmware update at [Dell support](https://support.dell.com)
* A link to the previous firmware upgrade at [LVFS](https://fwupd.org)
* The system

# Updating from an EXE without a capsule
While waiting for a firmware upgrade to be posted to LVFS if there is a time sensitive reason to update the firmware sooner, it is possible to install the firmware directly from the executable posted at https://support.dell.com on Linux systems.

## Prerequisites
* fwupd 1.0.9 or later installed locally
* The system must be booted in UEFI mode
* UEFI capsule updates must be turned on in BIOS setup.

To confirm these prerequisites, look in `# fwupdmgr get-devices` output for a device corresponding to System Firmware.  If either firmware prerequisite fails and you are using fwupd `1.3.x` or newer, you will be notified through the output.

## Performing the upgrade

To perform this upgrade, follow these steps:
1. Download the firmware upgrade executable to a local directory.
2. Clone fwupd locally
```
# git clone https://github.com/fwupd/fwupd
```
3. Run the contrib script to package the firmware into a capsule and install it.
```
cd fwupd
./contrib/firmware_packager/install_dell_bios_exe.py file.exe
```
4. Reboot your machine.
