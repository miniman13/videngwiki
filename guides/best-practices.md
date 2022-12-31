---
title: Industry Best Practices
description: 
published: true
date: 2022-12-31T06:43:46.440Z
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

Follow proper cable wrapping techniques to prevent damage to your cables and ensure they are properly organized.

Learn what hardward / software is standard in the industry where you work and try to get hands on experience.

Follow proper safety procedures when working with electrical and electronic equipment. This includes wearing protective gear, following proper lifting techniques, and knowing how to properly handle and use tools and equipment.

Know how to use your equipment's diagnostic and monitoring tools. This will help you troubleshoot problems and identify potential issues before they become major issues.


## Industry

This business is about relationships and it's a smaller industry than you think. Talk to people and make connections. Work hard in maintaining those relationships—those relationships are the way you get work.

Never burn a bridge.

Be confident in what you know, but also realize there are other people who know a lot too, so don’t get discouraged or annoyed when they actually do know more than you.
On the flip side, don’t get annoyed when someone doesn’t know as much as you do, and don’t be condescending or rude when explaining something, even if in your mind it’s “basic”.

Learning the way something is done now and sticking to that one way is dangerous, innovation is job security.

At the end of the day; it's not about the gear, it's about the product.

Don't be afraid to say you don't know something because it is painfully obvious when someone is faking it when it comes to the niche broadcast stuff.

Reading the manuals puts you ahead of 70% of folks (sometimes this includes the folks who work for the company who made the product).

## Video
 
Use 75 Ohm cables & BNC barrels for SDI.

When possible, genlock everything.

If using Blackmagic Design equipment, budget enough to buy a second unit for when the first one burns up. 🔥

## System Adminstration
Always reboot servers and workstations between installs/uninstalls/upgrades/patches/firmware.

Have a control of your updates / update cycles. The worst thing that could happen is a machine updating during a show or while on-air.

If possible avoid joining mission critical workstations to the domain (incase a DC doesn’t load/boot). If you can't avoid, make sure you have a local admin account.

Don’t make more than one large change at once to make rollback easier to determine.

Try to keep your devices at fixed IP addressing. Either set the IP statically or use a reservervation on your DHCP server.

Test your network cables. When possible certify them.

Don't mix your production protocols on the same VLAN. Seperate core services onto their own VLANs (ie Dante, NDI, ARTNET should all exist on their own network VLAN)

## Audio
Learn proper cable wrapping technique.

Do appropreate gain staging and leave headroom.

Invest in a good head amp.

It's recommended that phantom power be turned off when using ribbon microphones.

