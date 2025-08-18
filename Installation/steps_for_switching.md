# Installation Process

This document provides a high-level walk-through of the installation process. It
is meant to be unspecific.

## Preparation

It is important to get everything ready before committing to the installation
step. Here is my (not comprehensive and not detailed) checklist.

### Data Back-up (IMPORTANT)

No matter if you want to use a new drive for the OS or reuse an older drive, it
is important to make sure important data is backed up. It is best to have a
spare drive to either install Linux onto, or act as a temporary file depot. I
won't go into great detail on how to back up stuff, because everyone does it
slightly differently. But please consider the 3-2-1 rule, and please keep your
important data safe!

Personally, I will be installing CachyOS on a brand new NVNe SSD, and keep the
Windows drive in the near future in case I need to find anything.

### Hardware Preparation

Make sure a vacant drive exists to install the OS onto. Other than that, just
keep things stupid simple (KISS), with only strictly necessary components and a
few peripherals connected to the PC. Stuff can always be added on later.

### Installation Media

Having a working machine outside of the PC to install Linux on will be very
handy. Use it to make bootable installation media, and in the rare situation,
drivers. CachyOS should have pretty comprehensive driver support, especially
with the AMD GPU.

Obtain the latest installation image from the main site of CachyOS, then use
either Balena Etcher or Rufus to burn it to a USB drive.

## Installation

Be sure to reference the official installation guide. It is fine going with
default options. Try to stick with a more feature-rich file system like the
default Btrfs.

For desktop environment, choose anything that is stable and is Wayland-based to
better accommodate multi-monitor, high refresh rate setups.

## Post Installation

### Basic Checking

Once done with the installation process, make sure all peripherals work, all
monitors work, etc. Check system information to make sure all installed hardware
are detected. If anything is missing, use the internet to attempt
troubleshooting.

### Performing Updates

It is important that all packages, especially system packages, are up-to-date.
Refer to the package manager guides before doing this. Usually, drivers are
updated along side system packages, but just check them for good practices.

Depending on what updates are applied, a reboot might be necessary. Regardless,
the machine should be rebooted after system updates.

### Make Adjustment to Settings

Once the OS is up to date, it is OK to change a few settings here and there to
make the OS better align with user's habits and preferred aesthetics. Just be
sure to fully understand what each option does, especially when it comes to
options related to core OS functionalities.

### Installing Applications

After getting familiarized with the OS, use the terminal and package managers to
install the applications needed. Note that some packages might not be available
via official repos, and need to be obtained from alternative means. While doing
so, make sure the sources of the binaries are trustworthy. Never install
packages that seems dubious or cannot be verified!
