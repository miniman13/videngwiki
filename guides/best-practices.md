---
title: Best Practices
description: 
published: true
date: 2022-10-14T18:57:15.184Z
tags: 
editor: markdown
dateCreated: 2022-10-12T22:59:57.565Z
---

# Industry Best Practices

Document your work.

Backup early, backup often, backup multiple places.

Always have an exit plan. How do I recover from whatever I am doing if it doesn’t go to plan?
 
Always double check you're recording. If possible have a backup record. (As an excercise, consider how much it would cost / how much work it would take to re-create the program/performance if the record didn't happen or the record failed... it quickly becomes obvious it's worth a second glance to confirm).

Keep a copy of the previous software when upgrading. If possible archive every version– you never know when you need to roll back to support a device with incompatibiltes.

Learn proper cable wrapping technique.

## Video
 
Use 75 Ohm cables & BNC barrels for SDI.

When possible, genlock everything.

If using Blackmagic Design equipment, budget enough to buy a second unit for when the first one burns up. 🔥

## System Adminstration
Always reboot servers and workstations between installs/uninstalls/upgrades/patches/firmware.

Have a control of your updates / update cycles. The worst thing that could happening is a machine updating during a show or on-air.

If possible avoid joining mission critical workstations to the domain (incase a DC doesn’t load/boot). If you can't avoid, make sure you have a local admin account.

Don’t make more than one large change at once to make rollback easier to determine.

Try to keep your devices at fixed IP addressing. Either set the IP statically or use a reservervation on your DHCP server.

Test your network cables. When possible certify them.

Don't mix your production protocols on the same VLAN. Seperate core services onto their own VLANs (ie Dante, NDI, ARTNET should all exist on their own network VLAN)

## Audio

It's recommended that phantom power be turned off when using ribbon microphones.