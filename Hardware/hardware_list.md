# List of Hardware

Due to certain software compatibility issues, it is not possible for me to run
CachyOS exclusively. Here I note the machines I currently (or intend to) utilize
to cover all my use cases.

## Main Workstation

This is the workstation with the best hardware I have. This workstation runs
CachyOS. It is used for daily computing, and runs every game that supports Linux
(natively or via Proton).

### Main Workstation Hardware

- CPU: AMD Ryzen 7 7700X
- Motherboard: MSI MPG X670E CARBON WIFI
- RAM: DDR5 64 GiB @ 6000 MT/s
- GPU (Discrete): SAPPHIRE NITRO+ AMD Radeon™ RX 9070 XT GPU

## Windows Mini PC Mk.0

This is an old low power HP EliteDesk 800 G3 Mini that I got cheaply off eBay.
It runs a de-bloated version of Windows 11. It is used to run a couple of PC
ports of Asian mobile games that requires kernel level anti-cheat software
(mainly ACE by Tencent). No important personal data will be stored on this
machine.

This machine runs a Sunshine server and can be accessed via network from the
main workstation using Moonlight.

Due to it's old hardware and the lack of a discrete GPU, it cannot run any
graphics-heavy games (which is not the intended purpose of this machine
anyways).

### EliteDesk 800 G3 Mini Hardware

- CPU: Intel Core i5-7500T
- RAM: DDR4 32GiB @ 3200 MT/s
- GPU(Integrated): Intel® HD Graphics 630

## Windows Mini PC Mk.1

~~As of writing (June 5, 2025) this PC has not arrived yet.~~

I found it in a listing in CraftComputing's Discord Server. I am lucky to be
able to find such a rare variant. This is again an older Mini PC, specifically a
Dell OptiPlex 7090 Micro. This is a special version of this model featuring one
low-profile PCIe expansion slot.

The original plan was to install a low-profile, low power GPU that can be
powered solely by the PCIe bus. However, since I purchased a new GPU for my main
rig, I have the option to use the old 6800 XT for this mini PC.

To make it work, I purchased an external GPU dock from AOOSTAR with an OCuLink
port, as well as a PCIe to OCuLink adapter from Amazon. The reason for not using
Thunderbolt, a seemingly more popular protocol, is not as obvious initially. I
spent some time trying to hunt down a Dell branded Thunderbolt add-on card that
works with my particular mini PC. I ended up purchasing one that ended up being
not compatible. I bought the AOOSTAR dock without intending to use OCuLink, but
it turned out to be the saving grace. I'm not going to pretend I understand well
what OCuLink is or how it works exactly, so here is an
[Article](https://www.howtogeek.com/what-is-oculink/) that explains things
pretty nicely.

This machine will complement the main rig pretty well. I already installed a
couple games with aggressive anti-cheat software. Most plays pretty well.
Whether it can run some of my creator-related software well remains to be seen.

### OptiPlex 7090 Micro Hardware

- CPU: Intel Core i7-10700T
- RAM: DDR4 16 GiB @ 2666 MT/s
- GPU (via OCuLink): ASUS TUF GAMING Radeon™ RX 6800 XT OC Edition
