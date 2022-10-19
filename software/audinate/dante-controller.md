---
title: Dante Controller
description: 
published: true
date: 2022-10-19T02:48:47.836Z
tags: dante, audinate
editor: markdown
dateCreated: 2022-10-12T17:10:24.849Z
---

# Dante Controller
Dante Controller provides essential device status information such as device-level latency and clock stability stats, multicast bandwidth usage, and customized event logging, for devices on a Dante network.

## Product Page
https://www.audinate.com/products/software/dante-controller

## Download
https://my.audinate.com/support/downloads/dante-controller

Dante Controller is now download-gated behind an account sign in page.
The downloads of Dante Controller are walled-off behind a user sign in area. You can use this generic login if you'd like to avoid creating an account: 

Email: `audinate@gustr.com`
Password: `audinate`

# Under The Hood
What we know as Dante Controller is several executables (and several .jar files) bundled into a single application. The UI and Client is written in Java, with a native executable to communicate on the network level. The main logic of Dante Controller seems to be contained in `libDanteController.dylib`, located in the `Contents/MacOS` folder.

Dante Controller uses an executable called DanteControllerAgent to do the primary communication with the selected network interface, and the agent communicates back to the UI over WebSocket data.

![dante-controller-tech-overview.png](/dante-controller-tech-overview.png)

The DanteControllerAgent process will attempt to open two WebSocket ports in the 5xxxx range. The second address will have the port number incremented by one.

## MDNS
Dante Controller makes MDNS requests to `224.0.0.251` on port `5353` for the following queries:

`_netaudio-arc._udp.local`
`_dante-safe._udp.local`
`_dante-upgr._udp.local`
`default._dante-ddm-c._tcp.local`
`default._dante-ddm-c._tcp.local`

## DanteControllerAgent
DanteControllerAgent is a background executable that proxies the low-level network connection data to the Java UI / Application.

### Starting the Agent

`/Applications/Dante\ Controller.app/Contents/MacOS/DanteControllerAgent --interface=en1`

Which then gives a reply with the service type and port numbers. For example:

```json
{ "service":"websocket", "port":58637 }
{ "service":"webserver", "port":58638 }
```

### Arguments / Options

```java
DanteControllerAgent v4.6.0.8

Usage:
DanteControllerAgent <options>

Options:
--interface=<interface name>	The name of the interface to use.
--interface-index=<interface index>	Numerical index of the interface to use.
--webserver-port=<port>		[Optional] Use a specific port for the webserver.
--websocket-port=<port>		[Optional] Use a specific port for the websocket server.
--conmon-port=<port>		[Optional] The port to use for conmon.
--pid=<number>			[Optional] The process id of the parent process. The agent will terminate if the parent is not longer running.
--library-path=<string>		[Optional] The path to additional plugin libraries to search.
-?				Show this help
```


There are references to `LOG_CFG_FILE`,  `LOG_LEVEL` and `LOG_FILE` as hidden arguments.