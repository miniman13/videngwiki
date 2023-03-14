---
title: Genlock
description: 
published: true
date: 2023-03-14T04:47:15.247Z
tags: 
editor: markdown
dateCreated: 2022-12-16T06:19:27.051Z
---

The following is a synopsis from [a Reddit](https://old.reddit.com/r/VIDEOENGINEERING/comments/zmbei5/genlock_basics/j0adqy8/) post by [Eviltechie](https://old.reddit.com/r/VIDEOENGINEERING/comments/zmbei5/genlock_basics/j0adqy8/).

Genlock is a sync signal for video that lets all devices march in lock step. (e.g. they will all be creating video frames at the same moment in time).

There are two main types, blackburst and tri-level.

To generate your chosen signal(s), you need a sync pulse generator. This could be something basic like an AJA GEN10, or a full blown master clock like an Evertz 5601.

Genlock is considered an analog signal, so you need an analog distribution amplifier to distribute it.

All devices need a reference signal of some sort. If you don't supply it externally, they will usually free-run on an internal reference. Some may also derive sync from an incoming video signal.

To genlock a wild signal, you can use a frame synchronizer. A frame sync will buffer a few frames and add or drop them as necessary to bring the source in time.

Ideally, all inputs to a device and the device itself should be genlocked to the same reference source. In lieu of this, the device may have frame syncs built into its input stage. Lower level/prosumer gear often has this on all inputs. As you move up to mid-tier and higher level gear, this feature usually goes away as genlock is expected.

Your strategy in a small setup will often be to genlock what you can, and rely on internal framesyncs for the rest.

Things to watch out for:

Frame syncs inherently add delay. If every device has to frame sync its inputs, this can add up which is usually undesirable, especially in IMAG situations. If you can genlock everything, you can avoid this.

On some lower tier gear, you cannot disable the framesyncs, even if you can genlock the output of the device.

Even if you genlock everything, you may still have to adjust the sync offset on individual devices. This is most notable on graphics sources, as you may notice a small gap at the top or bottom of the image. To do this properly you need a real scope that can measure timing offsets.

Some devices lack this timing offset. You may have to steer an extra output of your sync pulse generator to handle this.

Genlock needs to be terminated. Each output that is in use should be terminated exactly once. Some devices will do this for you, some will have a switch, some will do it automatically when the loop through is not connected, and some will not do it at all and you will have to provide your own external terminator. You will usually need to read the manual to figure this out.

### More Reading:

[https://www.analog.com/en/analog-dialogue/articles/phase-locked-loop-pll-fundamentals.htmlx](https://www.analog.com/en/analog-dialogue/articles/phase-locked-loop-pll-fundamentals.htmlx)

[https://resi.io/blog/what-is-genlock/](https://resi.io/blog/what-is-genlock/)