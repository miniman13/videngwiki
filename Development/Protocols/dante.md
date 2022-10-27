---
title: Audinate Dante
description: 
published: true
date: 2022-10-27T03:45:37.918Z
tags: dante, audinate, audio-over-ip, video-over-ip
editor: markdown
dateCreated: 2022-10-12T22:25:53.263Z
---

# Dante

Dante is a combination of software, hardware, and network protocols that delivers uncompressed, multi-channel, low-latency digital audio (and now video) over a standard Ethernet network. Dante is an acronym for **D**igital **A**udio **N**etwork **T**hrough **E**thernet.

https://en.wikipedia.org/wiki/Dante_(networking)

# FAQ
## What is the minimum requirement for switches in a Dante network?

While Gigabit switches are recommended, 100Mbps switches may be used in limited scenarios.

For low channel count (<32) applications, a 100Mbps switch may be used as long as it supports proper QoS, and QoS is active. **The use of 100Mbps switches without QoS is not recommended or supported.**
For higher channel counts, Gigabit switches are essential. QoS is recommended for Gigabit switches on networks that share data with services other than Dante.

# Network Configuration

## IGMP Snooping
### IGMP v2 / v3 on macOS
IGMP is specified in two commonly used versions: v2 and v3. This difference is most easily seen on current macOS computers that use IGMP v3 on built-in Ethernet ports; these may fail when connected to IGMP v2 switches. An easy workaround is to use an Ethernet adapter, all of which use IGMP v2. https://www.audinate.com/blog/post/well-intentioned-mishaps-with-igmp-snooping

Alternately you can ‘Forward All’ multicast traffic to the Mac. In effect, that disables IGMP snooping for that port. However, assuming the Mac has a Gigabit port, you should be fine.

## Link-Local
> For Link-Local networks, Dante expects primary interfaces to use the 169.254.x.x range, and secondary interfaces to use the 172.31.x.x range.
{.is-info}

> The primary and secondary interfaces should not share a subnet or IP space. If a Dante device resets to factory default settings it may revert to "Daisy-Chain" mode – meaning it is now bridging your primary and secondary networks instead of offering redudancy - causing multiple interfaces to use the same IP address.
{.is-warning}

- IP addresses for each network interface must be unique.
- Dante Primary and Secondary networks must never be physically linked.
- Dante Primary and Secondary addresses must be in different subnets.
- Dante Primary will use the 169.254.x.x subnet when set to auto-configure. This is standard IPv4 protocol and therefore the same behaviour as the Connectivity network.
- Dante Secondary will use the 172.31.x.x subnet when set to auto-configure. This is still a private address within IPv4, and is not reserved exclusively for auto-configuration, making its use for secondary auto-configuration unique to Dante.
- In addition to being configured in different subnets, Dante Primary, Dante Secondary and Connectivity should typically be treated as three physically separate networks, with their own network hardware.

# Troubleshooting
## Using Wireshark to Troubleshoot Dante Issues
### Filters

#### Filter Multicast

`(eth.dst[0] & 1)`

#### Filter to Port

`udp.port == 4440`


# Reverse Engineering

> Some details on this page are derrived from packet inspection or other reverse-engineering techniques and are not officially released from Audinate.
{.is-warning}



## Ports

### 8700 (UDP)

- Sample rate
- Level control
- Preferred Encoding
- Device Identification (Flash Port Light)

### 4440

- Get/set subscriptions
- Device latency
- Set/reset channel name
- Rename device

### 5353 (MDNS)

- Read device encoding
- Read device sample rate
- Read device latency
- Enumerate channel count
- Device discovery
- Device model
- MAC address
- Device manufacturer
- Device version

### 5353 (244.0.0.251 Multicast)