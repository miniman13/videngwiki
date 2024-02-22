---
title: Studio Converter
description: Blackmagic's Camera Control Units
published: true
date: 2024-02-22T07:24:00.820Z
tags: 
editor: markdown
dateCreated: 2022-11-28T11:17:15.564Z
---

>Unlike a traditional broadcast chain, Blackmagic uses the ATEM to embed controlling signals  (such as lens, brightness, and color controls) on the PGM feed.
{.is-info}

# 2021 Blackmagic Studio Converter

The 2021 Blackmagic Studio Converter ($955 starting price) is a 10G Ethernet (possibly TICO-based) CCU for the Blackmagic Studio Camera 4K Pro and Blackmagic Studio Camera 4K Plus. 

![](/hardware/blackmagic/studioconverter/2021blackmagicstudioconverterdiagram.png)

# 2018 Blackmagic Studio Fiber Converter

The Blackmagic Studio Fiber Converter ($2,995 starting price) is a 12G SMPTE hybrid fiber CCU for the Blackmagic Camera Fiber Converter. The optical I/O is not implemented. 

> The DB25 tally requires embeded ancillary data on the Return 1 SDI (via an ATEM) in order to override. A possible workaround is to loop the output from a BMD camera (which has ancillary data) into Return 1 or use the BMD Arduino Shield.
{.is-warning}

> According to BMD, the SMPTE hybrid fiber line uses 10G "IP video" networking. It is probably TICO and is definitely compressed to shove 12Gb/s of data down a 10G link. [Source](https://youtu.be/6-pcQ4PpzPs?si=j4mSkX6EuXCHTfN9&t=3209)
{.is-info}


![](/hardware/blackmagic/studioconverter/2018blackmagicstudiofiberconverterdiagram.png)

# 2013 ATEM Talkback Converter 4K

The ATEM Talkback Converter 4K ($2,495 starting price) is an 8x12G-SDI optical converter and talkback embedder. It does not come with SFPs.

"Talkback and tally, along with video, are sent to each camera over the SDI program return. The ATEM Talkback Converter takes advantage of the 16 channel SDI audio standard and embeds the talkback into rarely used channels 15 and 16. That means customers don’t need any extra cables to add talkback and tally to their production."

![](/hardware/blackmagic/studioconverter/2015atemtalkbackconverter4kdiagram.png)

# 2013 ATEM Studio Converter 2

The ATEM Studio Converter 2 ($1,995 starting price) is a 6G-SDI optical converter with 4x6G-SDI outputs and talkback embed. 

![](/hardware/blackmagic/studioconverter/2013atemstudioconverter2diagram.png)

# 2011 ATEM Studio Converter

The original ATEM Studio Converter (€1395 starting price) is a 4x optical converter that outputs whatever is in the optical in onto the HDMI out and sends the PGM In (HD-SDI) on the optical in, but can be individually overridden via each respective SDI IN. It comes with SFPs and talkback embed. 

![](/hardware/blackmagic/studioconverter/2011atemstudioconverterdiagram.png)