---
title: Useful FFMPEG Commands
description: because we will never remember all the options
published: true
date: 2022-10-15T20:40:42.535Z
tags: foss, open source, ffmpeg, software
editor: markdown
dateCreated: 2022-10-15T18:39:11.751Z
---

Useful FFMPEG Commands

Record HLS Stream from Beginning

`ffmpeg -live_start_index -99999 -i 'http://domain.com/hls/master.m3u8' -c copy localFile.mkv`

Timeslip one Decklink to Another

`ffmpeg -f decklink -audio_input embedded -channels 16 -i 'DeckLink SDI (1)' -vcodec libx264 -crf 25 -preset ultrafast output.mkv`

`ffmpeg -re -i output.mkv -f decklink -pix_fmt uyvy422 'DeckLink SDI (2)'`

Mirror HLS to directory via FTP: 

```plaintext
ffmpeg -i http://remote.com/hls/segs/master.m3u8 -c:a copy -hls_time 9 -hls_list_size 3 -hls_wrap 0 -start_number 0 -hls_allow_cache 0 -segment_list_flags +live -hls_flags delete_segments ftp://ffmepg@domain.com:password@ftp.domain.com/master.m3u8
```