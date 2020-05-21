![PVEKCLEAN Logo](https://repository-images.githubusercontent.com/265764497/3b460400-9b98-11ea-9e5e-f74e8d76bb76)

Clean up old and unused PVE kernels from your ProxmoxVE hypervisor

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)

### What is PVE Kernel Cleaner?

PVE Kernel Cleaner is a program to compliment the [ProxmoxVE](https://www.proxmox.com) hypervisor environment.  As the PVE kernels are upgraded, they aren't automatically uninstalled, and accumulate in your root or /boot partitions.  Eventually this can cause storage space issues, filling up your partition with old kernel images.

PVE Kernel Cleaner was created to fix this problem, allowing you to easily purge the old kernels filling /boot. 

## Example Usage

![PVEKCLEAN Example](https://jordanhillis.com/images/github/pvekclean/pvekclean_example3.png)

## Features

* Removes old PVE kernels from your system
* Schedule PVE kernels to be automatically removed on a regular basis
* Run a simple pvekclean command for ease of access
* Checks health of boot disk based on space available
* Tested on ProxmoxVE 6.x

## Latest Version

* v1.4

## Prerequisites

PVE Kernel Cleaner requires cron for scheduled kernel cleaning.  This comes installed in PVE by default; however if you've removed it, you can reinstall it with:

```bash
# apt update && apt install cron
```

## Instalation and Updating

To install or update PVE Kernel Cleaner, simply download and run it:

```bash
wget https://raw.githubusercontent.com/rhyven/pvekclean/master/pvekclean.sh
chmod +x ./pvekclean.sh
./pvekclean.sh
```

## Usage

Example of usage:
```
 pvekclean [OPTION]

-f		--force				Remove all old PVE kernels without confirm prompts
-s		--scheduler			Have old PVE kernels removed on a scheduled basis
-v		--version			Shows the current version of pvekclean
-r		--remove			Uninstalls pvekclean from the system
-h		--help				Show these options
```

## Developers

* **Jordan Hillis** - Original Developer
* **Rhyven** - Contributor, 2020
* **PeterDaveHello** - Contributor, 2019

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* This program is not an official program by Proxmox Server Solutions GmbH
