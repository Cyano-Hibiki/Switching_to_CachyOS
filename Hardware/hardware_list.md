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
- GPU (Discrete): AMD Radeon RX 6800XT

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

## Windows Mini PC Mk.1 (Incoming)

As of writing (June 5, 2025) this PC has not arrived yet. I found it in a
listing in CraftComputing's Discord Server. I am lucky to be able to find such a
rare variant.

This is again an older Mini PC, specifically a Dell OptiPlex 7090 Micro. This is
a special version of this model featuring one low-profile PCIe expansion slot. I
intend to install a Yeston RTX 3050 Low Profile into the slot to test if it will
handle slightly more demanding games. However, my hopes are low, since most of
the discussions I found online have been suggesting that the power supply via
the PCIe slot will not be able to handle the 3050 with a 75W TDP. The slot was
originally populated with an RX 640 with 4GB GDDR5 VRAM at 50W TDP.

Currently, several possible solutions are present. I will be testing out the
3050 since the card is relatively cheap even for brand new ones. If it won't
work or turns out being unstable, then I will try an AMD 6400 Low Profile card.
Again, this is a cheap card and for it's price on eBay, I don't really mind
risking buying used. Another candidate is an Intel Arc A310. However, the
performance on that card is quite handicapped, so it will be the last option for
something that fits inside the chassis.

There is also the option to install a Thunderbolt adapter card, and hook up an
external GPU chassis. A quick search on eBay suggests that a bare bone eGPU
chassis can be obtained for 150 to 250 USD, while a used Dell Thunderbolt 3
expansion card is less than 80 USD as of June 2025. I will also need a PSU for
the eGPU chassis. This is definitely the most expensive solution, but there
might be a higher chance of success in terms of getting better graphics
performance.

### OptiPlex 7090 Micro Hardware

- CPU: Intel Core i7-10700T
- RAM: DDR4 16 GiB @ 2666 MT/s
