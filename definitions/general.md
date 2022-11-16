---
title: Definitions
description: Some words can be confusing
published: true
date: 2022-11-16T06:34:14.857Z
tags: 
editor: markdown
dateCreated: 2022-10-12T06:01:50.852Z
---

# Glossary
Some of the words and acronyms can be confusing, hopefully this list helps you work it out. 

Because we're all in different places and doing different styles of shows some of these might not be entirely correct, but it's a place to start if you don't know what something means.

When there's multiple things that mean the same, or one thing that means many different things in different contexts, try and add all the definitions, and if you see something that you feel is wrong, discuss it with others and either update it or add an alternative definition.

## 2110
(*Pronounced twenty-one ten*) the SMPTE standard for professional media over managed IP networks. Typically refered to in a context of replacing serial digital interface ([SDI](#SDI)) with IP.

## ADA
Audio or [Distribution Amplifier](#DA). Uncommon: Analog Video Distribution Amplifier.


## ASI
Asynchronous Serial Interface. Method of carrying MPEG transport streams over coax or fibre.

## Aston
See [graphics](/en/definitions/graphics) definitions
Aston Broadcast Systems is a developer of PC-based graphics generation software. The word "aston" is often used generically to refer to the text/graphics themselves, especially in UK broadcasting. See also [CG](#CG), [Chyron](#Chyron), [Lower Thirds](#Lower_Thirds).


## Birdbeater
Placeholder content sent to transmission in order to positively prevent [Program](#Program) content from accidentally being sent to [transmission](#Transmission). May refer to the actual content itself or to an automated process which interrupts program content. "Bird" refers to a satellite. Example: ESPN may require transmission of a birdbeater when program is not on air in order to prevent hot mics from going to air. 

## BP
Short hand for beltpack.

## Cart
Cart, or Cart Machine, refers to a hardware or software device used for audio playback, or to the input/source on a mixer/switcher/router designated for audio playback. Short for "Cartridge Machine," a tape-based playback device with a high channel count and relatively short playback time. Used primarily for jingles, bumpers, ads, and sometimes full songs. See also [Cartwall](#Cartwall)

## Cartwall
Software for one-shot playback of audio samples. The software may have additional features intended to make royalty payments on licensed content easier, such as timestamped logs recording the number of times a piece of content is played. See also [Cart](#Cart)

## CG
See [graphics](/en/definitions/graphics) definitions

Acronym for "Character Generator" or "Computer Graphics" which defines a machine or service that generates text and images to be used live on air. 

Examples
- Ross Xpression
- Vizrt
- CasparCG
- ProPresenter
- [Aston](#Aston) 
- [Chyron](#Chyron)

See also [Lower Thirds](#Lower_Thirds)

## Chyron
See [graphics](/en/definitions/graphics) definitions

Manufacturer of computer graphics generators. Name is often used as a generic reference to computer graphics. See also [Aston](#Aston), [CG](#CG), [Lower Thirds](#Lower_Thirds)

## Converter
Anything that processes and changes at least one of the following about a signal (but no limited to): formats, framerates, standards, color spaces, dynamic ranges, and resolutions. Typically hardware.

## DA
A Distribution Amplifier accepts a single input signal and provides the same signal to multple isolated outputs.

## Dante

Dante is a combination of software, hardware, and network protocols that delivers uncompressed, multi-channel, low-latency digital audio and video over a standard Ethernet network. Dante is an acronym for **D**igital **A**udio **N**etwork **T**hrough **E**thernet. Most of the time when people refer to Dante, they're referring to the audio related equipment or protocol.

## DCDA
Down Converting [Distribution Amplifier](#Distribution_Amplifier)

## Deck
*needs more details*

## De-embedder
Most frequently refers to a device which takes an input with multiple types of data and extracts one or more types for isolated output. Should also have a "loop output" which passes the input signal unaltered. For example, an SDI to Analog Audio De-embedder should have an SDI video input, an SDI video output, and between 1 and 16 analog audio outputs. 

## DUC
Down, Up, Cross. See [Up, Down, Cross](#up-down-cross)

## DVE 
Digital Video Effects (sometimes Digital Video Engine). Most often refers to resizing, repositioning, or distorting an image. May also refer to the hardware or software processor dedicated to applying the effect. 

## Embedder
Most frequently refers to a device which takes two or more 

## Frame Sync
*needs more details*

## Genlock
The state of equipment being locked to a frame. *Reference signal* (the signal that equipment locks to for timing) is often wrongly referred to as "genlock". See the Reference definition and Genlock & Timing info page for more details. TBD.

## GPI/GPO/GPIO
General Purpose Input, General Purpose Output, or General Purpose Input/Output. Often refers to bare wire connections or ports on a device allowing for serial communication or contact closure. Devices may have only GPI or GPO, but GPIO as a generic term may be used to refer to either/both. 
Should be accompanied by a legend called a "Pinout" to indicate the function of each pin. Pinouts may be found in manufacturer documentation, but may also be printed directly on the device. 

## Hybrid Router
A [router](#Router) that routes multiple levels of signals, such as Audio, Video, Ancillary, Time Code, etc.

## Ingest
*needs more details*

## Jackfield
See: [Patchbay](#patchbay). A panel, often in a rack, where multiple physical signal paths are terminated. A jack may also be called a port or spigot, meaning a place where a plug is inserted. 

## Lower Thirds
See [graphics](/en/definitions/graphics) definitions

Generic term used to refer to graphics/text overlay on the lower third of an image. May also refer to graphics/text overlaid in other areas of the image, but those may have more specific names such as: 
Hat - typically placed across the top of the image
Ticker - a scrolling list which may appear anywhere in the image
Bug - a small, usually static graphic which most frequently appears in the corner of the image.

See also [Chyron](#Chyron), [Aston](#Aston)

## Master Control
Technical hub which is the final point in the broadcast chain before an over-the-air transmitter or cable/satellite providers. Typically refers to a physical control room or truck within a larger complex of control rooms. 

## ME
Mix/Effect. Refers to the scope of processing within a video switcher focused on a singular program output and one or more preview/preset outputs, clean feeds, etc. Some manufacturers such as Ross Video have MiniME's which are not as powerful as full ME's. Most consumer-grade video switchers, such as the ATEM Mini or Roland V-4EX, have a single ME. Many software-defined video switchers have additional ME's either included or available for license. 

An M/E comprises of a program bus, preview/preset bus, select bus, transition block, and typically, keyers. An AUX output is not typically considered an ME since it is frequently limited to hard cuts and does not "mix" video sources. 

## Melt
*needs more details*

## MIP
Multi-Image Processor. Uncommon term for a multiviewer, may be manufacturer-specific. See [Multiviewer.](#multiviewer)

## Multiviewer
A generated display "mosaic" showing many small boxes with video signals displayed inside them. Also known as MIP, VIP (Evertz term), and Multiview/MV. Each individual box may be called a [PiP](#PIP), which stands for "Picture-in-picture."

## OBS
**O**pen **B**roadcaster **S**oftware is a digital encoder and general purpose livestreaming application. For more information see [OBS Studio](/en/software/obsproject/obs).

## OpenGear
A frame and card standard created by Ross. The frame provides networking, control, and power to slots that can accept Open Gear cards. OpenGear X (OGX) is the newer standard with more power than OpenGear 3.

## NMOS
*needs more details*

## Partyline
A group audio line within a production intercom system where all members of the partyline can hear and talk to all members within the partyline non selectively.

## Patchbay
A rackmount interface that allows you to redirect video or audio signals from an input to an output. They come in "Normalled," "Half-normalled," and "Un-normalled/Non-normalled" versions. 

Normalled patchbays internally connect the top row to the bottom row by default unless patched with a cable, which is called "breaking the normal." I.e., They are "normally" connected ;)

In a half-normalled patchbay, inserting a cable into the top row "taps" the signal, meaning it does not interrupt the flow from the top rear connection to the bottom rear connection. However, inserting a cable into the bottom row *does* interrupt the rear connections. (Note: half-normalled patchbays are uncommon in video and are more likely to be found in audio)

Un-normalled/Non-normalled patchbays have no internal connections and require the addition of a patch cable in order to complete a signal path. See also [Jackfield](#Jackfield)

![patchbay.png](/patchbay.png)

## PIP
Picture-in-picture. May refer to either a single box within a [Multiviewer](#Multiviewer) or more correctly, the use of a [DVE](#DVE) to superimpose a small source on top of a larger image. A "picture inside of a picture".

## Program
May refer broadly to the primary content intended to be viewed by the audience, or more specifically to the main output of one or more ME's (Mix Engines) within a video switcher. 

## Rattler
Originally a model of Telecast SDI over fiber optic conversion system, has become slang for any SDI over fiber conversion system.

## RCP
*needs more details*

## RFQ
**R**equest **F**or **Q**uote: a document that details pricing options for services or product(s). In Production, an RFQ is often used during the procurement process.

## ROI
Region of Interest. Refers to a selected part of a raster. Typically as a term for checking pixel values in a given "region" or scaling to a "region of interest" in the case of an ROI converter.

## Router
A (typically) hardware device with either hardware or software control which takes multiple inputs/sources and routes them to multiple outputs/destinations. May route multiple levels (signal types). The act of routing a source to a destination is called "taking" a route. Some routers may take multiple routes at once by means of a macro or [Salvo](#Salvo).

The router may or may not be clean-switching, meaning the signal may or may not lose sync and drop when a new route is taken. Clean-switching routers typically add delay/latency in order to synchronize signals in a buffer. 

## Scan Converter
A device that converts computer signals into broadcast standard signals. Originally, this was for computer signals to analog TV signals, now it usually refer to any converter (including throwdown converters) that converts 60Hz to 59.94Hz and the like.

## SDI
Serial Digital Interface. Refers to a transport defined by SMPTE 259M, SMPTE 292M, and SMPTE 424M providing for transmission of digital video with embedded audio and ancillary data, most frequently over coaxial cable or fiber optic cable. 

## Slate
*See graphics definitions.*

## Switcher
*needs more details*
See also [VMU](#VMU), [Vision Mixer](#Vision_Mixer), [TD (Technical Director)](#TD_(Technical_Director))

## Tally
Refers to the indicator (and respective signal) that tells the operator their input (typically a camera output) is "live" on the switcher. Red indicates the input is on program, and green indicates that the input is on preview.

Tally *signals* are generated by the switcher usually with contact closures or in the case of ATEMs, digitally on the SDI PGM feed ancillary data. Tally *indicators* are usually dots displayed on a viewfinder and/or actual lights that illuminate the appropriate color.

## Tally Whack
*needs more details*

## Tape Machine
Used to refer to any device that can record or playback video regardless of whether it is recording to a linear or non-linear format. Tape Machines are not typically referred to by their engineering names, but are given names that are easier for the production staff to know what is on the machine or refer to it in their production. 

<details>
<summary>Expand to see some common names</summary>
    Red  <br>
    Blue  <br>
    Gold <br>
		Silver <br>
		Black <br>
		Laser <br>
		Elvis <br>
		Cash <br>
		Money <br>
		A <br>
		B <br>
		C <br>
		D <br>
		X <br>
		Y <br>
		Z <br>
		Disk <br>
		(The names of the producers kids)
</details>

 See also:
- [VTR](#VTR)
- [Deck](#Deck)
- [Replay](#Replay)
 {.links-list}

## TD (Technical Director)
The person in a control room tasked with operating the video [switcher](#Switcher).

## Throwdown
A small, usually handheld size, device that can process a signal of some sort. May refer either to a device which cannot be rackmounted or to a rackmounted device being used without a rack. Some common throwdows are:
- SDI -> HDMI
- HDMI -> SDI
- SDI Up/Down/Crossconversion
 
## Track
*needs more details*

## TX
See: [Transmission](#transmission)

## Transmission
Transmission can refer to the act of actually transmitting a signal over the air, or in an OB truck, the signal that leaves the truck to be distributed. 

## ISO
Isolation: A dedicated record of a specific source. Also used in the context of "Director ISO" and "Producer ISO" which are dedicated router outputs assigned to a router panel in front of those positions. Commonly used by a producer to show talent specific content without using the program monitor in the booth.

## UMD
Under Monitor Display. Source and operator name are common information displayed in a UMD. Modern UMD's are no longer physical devices below the monitors, but digital elements on a rendered multiviewer.

## UDX
Up, Down, Cross. See [Up, Down, Cross](#up-down-cross)

## Up, Down, Cross
Up, Down, Cross converter. A converter that can scale the raster up, down, and adjust temporal resolution (framerate).

## VDA
Video [Distribution Amplifier](#DA)


## VMU
Vision Mixer Unit, common parlance for users not in the United States. See [Switcher](#Switcher), [Vision Mixer](#Vision_Mixer)

## Vision Mixer
Common parlance for users not in the United States. Refers either to a video [switcher](#Switcher)/[VMU](#VMU), or to the person operating the video [switcher](#Switcher) who is more commonly known in the US as the [TD (Technical Director)](#TD_(Technical_Director)).

## VTR
Refers to a stand-alone record/playback device such as a Hyperdeck, Shogun Studio, or even a Betacam Tape Deck.

