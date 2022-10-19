---
title: NDI
description: 
published: true
date: 2022-10-19T03:08:16.020Z
tags: ndi
editor: markdown
dateCreated: 2022-10-14T05:35:10.566Z
---

# Newtek NDI
NDI stands for **N**etwork **D**evice **I**nterface.

https://en.wikipedia.org/wiki/Network_Device_Interface

Also see NDI page
https://videng.wiki/en/software/VizRT/NDI

## Ports

| Port number | Type | Use |
| --- | --- | --- |
| 5353 | UDP | This is the standard port used for mDNS communication and is always used for multicast sending of the current sources onto the network. |
| 5959 | TCP | NDI Discovery Server is an optional method to have NDI devices perform discovery. This can be beneficial in large configurations, when you need to connect NDI devices between subnets or if mDNS is blocked. |
| 5960 | TCP | This is a TCP port used for remote sources to query this machine and discover all of the sources running on it. This is used for instance when a machine is added by an IP address in the access manager so that from an IP address alone all of the sources currently running on that machine can be discovered automatically. |
| 5961 and up | TCP | These are the base TCP connections used for each NDI stream. For each current connection, at least one port number will be used in this range. |
| 5960 and up | UDP | In version 5 and above, when using reliable UDP connections it will use a very small number of ports in the range of 5960 for UDP. These port numbers are shared with the TCP connections. Because connection sharing is used in this mode, the number of ports required is very limited and only one port is needed per NDI process running and not one port per NDI connection. |
| 6960 and up | TCP/UDP | When using multi-TCP or UDP receiving, at least one port number in this range will be used for each connection. |
| 7960 and up | TCP/UDP | When using multi-TCP, unicast UDP, or multicast UDP sending, at least one port number in this range will be used for each connection. |
| Ephemeral | TCP | Legacy to NDI v1 - The current versions (4.6 and later) no longer use any ports in the ephemeral port range. |