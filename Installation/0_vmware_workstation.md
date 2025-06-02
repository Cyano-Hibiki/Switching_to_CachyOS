# Testing with VMware Workstation

## Motivation

In order to figure out the installation process and test out some applications without interrupting my current workflow, I decided to install CachyOS in a VM. The use of **VMware Workstation Pro 17** is only motivated by the fact that I have it installed and has a license to the software.

## Installation Process

### Setting up the VM

- Right click in Library and select **New Virtual Machine**.
- Choose **Custom (advance)**.
- Stick with default compatibility.
- Choose installer image.
- Choose **Linux**, then **Other Linux 6.x kernel 64-bit**.
- Rename the VM to something like `CachyOS`.
- Change number of processors to `1` and number of cores to `4`.
- Change memory to `16 GB` (`8 GB` probably works).
- Use default NAT.
- Use recommended I/O controller.
- Use default disk type.
- Create a new virtual disk.
- Change disk size to `64 GB`, and choose **Store virtual disk in a single file**.
- Use default disk file location.
- Finish.
- Optionally turn on **Accelerated 3D graphics** and specify a monitor resolution.

### Installing CachyOS
- Once the VM is created, turn it on.
- Follow the boot option menu and choose the first option to enter the live CD.
- Upon booting up, change the session to **Wayland** and log in with no password.
- The intro screen has a button to install CachyOS, click that.
- Follow the installation guide and finish up the installation.