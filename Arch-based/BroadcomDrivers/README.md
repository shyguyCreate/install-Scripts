# Broadcom Package Driver for Arch-based distros

Download script and install script for packages needed by the **Broadcom wireless network device** based on information provided in the [Arch wiki](https://wiki.archlinux.org/title/broadcom_wireless).

### Download packages for driver
Packages are downloaded using `pacman` but not installed, instead they are saved to `$HOME/BroadcomPackages` to use them for an offline installation.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/shyguyCreate/install-Scripts/main/BroadcomDrivers/Arch-based/broadcomDownload.sh)"
```

### Install packages for driver
Packages are retrieved from `$HOME/BroadcomPackages` and installed using `pacman`. And modules are removed and loaded for the driver to work.
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/shyguyCreate/install-Scripts/main/BroadcomDrivers/Arch-based/broadcomInstall.sh)"
```

-----------

***Note:*** the scripts are separate because packages are meant for an offline installation in another device.

> If you are looking to install the packages in the same device, just run `sudo pacman -Sy base-devel linux-headers broadcom-wl-dkms` in the terminal.
