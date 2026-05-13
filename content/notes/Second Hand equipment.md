+++
draft = false
title = 'Building a secondhand homelab [Part 1]'
weight = 1
tags = ["development","2026"]
showtoc = false
author= [""]
showCodeCopyButtons = false
ShowPostNavLinks = false
ShowBreadCrumbs =false
ShowCodeCopyButtons = false
ShowWordCount = false
ShowRssButtonInSectionTermList = false
UseHugoToc = false
disableSpecial1stPost = false
disableScrollToTop = false
comments = false
hidemeta = false
hideSummary = false
tocopen = false
ShowReadingTime = false
ShowShareButtons = false
+++


My self-hosted journey v2 has begun and first things first i had to collect oldish pieces of hardware to build my cluster.
In the v1 i didn't focused myself that much on hardware specs, i was younger and i was too electrized by the idea of having my
internal server machine, i ended up picking an old mini HP powered by a decade yo Intel i3 CPU. And of course it was a crap. I mean as a tiny docker server with was good but for Proxmox, it wasn't even able to run VMs.

This time, hardware analysis has been widely carried out as i started identifying the best socket and configurations for my needs, considering i was on budget and second hand platforms are often still expensive. Vinted, Ebay, Wallapop and local market websites were my main sources for equipment, i did tons of scrolling, kilometers of saved search and luckily every now and then some bargain appeared and thanks to a couple of gentlemen i found, i was able to get them for an incredible price per value. 

My requirements are simple:

- <b>Form factor: </b> I have a tiny rack hence small form factor (SFF) was a mandatory choice.

- <b>CPU/GPU</b>: Intel up from 6 or 7th gens, for example i5-6500,i5-7600,i5-8500, i7-6700,i7-7700 and so on. For AMD i was more or less interested in any recent Ryzen architecture. In short, prosumer processing units with 65W TDP. 

- <b>RAM</b>: nothing less than 8GB DDR4 with a max amount of 64 GB. 

- <b>PCIe</b>: luckily, since SFF comes from ex enterprise or business environment, the biggest part of them are equipped with 2x PCIe slots
and this is really usefull to upgrade them to some Intel 2.5Gbps ethernet card.

- <b>Storage</b>: My ideal configuration was haveing at least 2x SATA and 1x NVME, first ones for ZFS mirror the NVME for OS.

### Storage

Surfing through used SSDs was a bit of a nightmare but i luckily learnt a lot about them. Indeed i stumbled upon a guy selling
enterprise SSDs and if you look at the specs they are totally different from consumer ones. I wasn't that much happy about the idea
of building my system on top of used storage but reddit and communities opinions made me change my mind. Enterprises disks are made to resist to hundreds of terabytes or petabytes of written data with best technology on the market and if you are lucky to find
"old" but lightly written SSDs you're all set. Luckily, tools such as CrystalDisk can deeply analyze disk status and you can 
quick check the health of the hardware. 

- Power On Hours 
- Power on Count
- Reallocate NAND Block Count
- Total Host Writes
- Health

Are some of the parameters i checked on to evaluate the status and the "interest" factor of an used disk.

My storage configuration for each node is composed by:

- Internal NVME for OS and .ISO images
- Mirrored 1 TB SSD for ZFS

Luckily, i ended up buying dismissed enterprise SSDs from datacenter, Intel and Samsung with a unsignificant PoH value and they are going to be perfect for my ZFS setup.

### Network

All of my equipments came with the standard 1G LAN network so the PCIe expansions allowed me to extend the connectivity to a 2.5G NIC.

Unfortunately, i did it wrong by choosing a Realtek card over an Intel one and since the Realtek driver doesn't works well with auto-speed negotiation, i need to switch to an Intel card ASAP to have the best network performances.

### Operating System

Proxmox is simply amazing for these kind of setups. It has an amazing community, tons of documentations, it's very stable and quite customizable.




