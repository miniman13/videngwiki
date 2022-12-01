---
title: Dante Virtual Soundcard
description: 
published: true
date: 2022-12-01T08:10:36.100Z
tags: dante, audinate
editor: markdown
dateCreated: 2022-10-12T17:02:54.580Z
---

# Dante Virtual Soundcard

Dante Virtual Soundcard is a simple, easy-to-use software application that turns a Windows or Mac computer into a Dante-enabled device, enabling you to instantly connect to any Dante network. Dante Virtual Soundcard uses your computer’s Ethernet port to communicate with other Dante-enabled devices on the network.

## Product Page
https://www.audinate.com/products/software/dante-virtual-soundcard

## Download
https://my.audinate.com/support/downloads/dante-virtual-soundcard

## Activation
> Each Dante Virtual Soundcard license can be activated four times before you receive an error (“The license has been activated too many times”) preventing further activiations.
{.is-info}


## Networking
Dante Virtual Soundcard only works on untagged VLANs. If your network interfaces has multiple VLANs trunked, Dante Virtual Soundcard will only communicate on the untagged VLAN.

### IGMP Snooping Forwards All on macOS
macOS machines running Dante Virtual Soundcard will likely lose clock-sync and mute when IGMP Snooping is engaged on many switch manufacturers. The macOS and many switch configurations do not refresh the Time-To-Live for multicast subscriptions, and thus the clock falls silent. You’ll know this is the case if Dante Controller shows “Listening” status. To address this manually forward multicast traffic to the ports the Mac is using. Related to https://serverfault.com/questions/819793/os-x-network-stack-ignores-igmp-membership-queries

### 10Gb Ethernet on macOS
Dante Virtual Soundcard (transmission) does not work on any 10Gb ethernet ports on macOS. You'll have to use a Thunderbolt to 1Gb Ethernet adaptor if you're using a machine that has a 10Gb ethernet port. http://duc.avid.com/showthread.php?t=410371
The reason for this is the 10Gbps Ethernet port on macOS does not support PtP (Dante Clock) correctly, rendering it useless for Dante. This is an Apple hardware/driver issue which also impacts other protocols that need PtP clocking, and with nothing Audinate can do to fix it. (According to Audinate, Apple fixed this issue in macOS 12 Monterey)
