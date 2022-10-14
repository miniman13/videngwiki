---
title: Makito X Encoder
description: 
published: true
date: 2022-10-12T23:22:34.644Z
tags: encoder, rtmp, srt
editor: markdown
dateCreated: 2022-10-12T17:22:22.236Z
---

# Makito X Encoder
The Makito X is an ultra compact SDI or DVI H.264 encoding appliance with optional HEVC encoding support, internal and/or removable storage.

# Models
### Makito X Single SDI
![haivision-makito-single-sdi.png](/haivision-makito-single-sdi.png)
### Makito X Dual SDI
![haivision-makito-dual-sdi.png](/haivision-makito-dual-sdi.png)
### Makito X DVI
![haivision-makito-dvi.png](/haivision-makito-dvi.png)
### Makito X (Harsh)

# Documentation
https://doc.haivision.com/MakitoXEnc2.5.2

## Factory Reset
To reset the Haivision Makito use a paper-clip to hold down the reset button on the encoder. After ~5 seconds the status light will turn red and the device will reboot with a factory-default configuraiton. The encoder can remain powered the entire duration of the factory reset.

> When factory-reset, Haivision Makito X has a default username of `admin` and a default password of `manager`.
{.is-info}

Once reset the Makito will reboot with a default IP address of `10.5.1.2` with a subnet mask of `255.255.0.0` and a gateway of `10.5.0.1`.

## Undocumented API Endpoints

| URL | Requires Auth | Description | Type |
| --- | --- | --- | --- |
| /apis/system_info | NO | Returns a list of capabilities of the system |  |
| /apis/banner | NO | Returns the login text/banner message |  |
| /apis/authentication |  |  |  |
| /apis/policies |  |  |  |
| /apis/talkback |  |  |  |
| /apis/sap/0 |  |  |  |
| /apis/streams | YES |  |  |
| /apis/status |  |  |  |
| /apis/authentication |  | Returns a response if you’re authenticated.  | GET |
| /apis/authentication |  | Sends --data-binary with username and password to auth | POST |
| /apis/streams/1/pause | YES | Pauses stream output | PUT |
| /apis/streams/1/resume | YES | Resumes the stream output | PUT |