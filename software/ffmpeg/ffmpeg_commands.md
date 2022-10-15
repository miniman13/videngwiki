---
title: Useful FFMPEG Commands
description: because we will never remember all the options
published: true
date: 2022-10-15T20:43:00.131Z
tags: foss, open source, ffmpeg, software
editor: markdown
dateCreated: 2022-10-15T18:39:11.751Z
---

Useful FFMPEG Commands

### Record HLS Stream from Beginning

`ffmpeg -live_start_index -99999 -i 'http://domain.com/hls/master.m3u8' -c copy localFile.mkv`

### Timeslip one Decklink to Another

`ffmpeg -f decklink -audio_input embedded -channels 16 -i 'DeckLink SDI (1)' -vcodec libx264 -crf 25 -preset ultrafast output.mkv`

`ffmpeg -re -i output.mkv -f decklink -pix_fmt uyvy422 'DeckLink SDI (2)'`

### Mirror HLS to directory via FTP: 

`ffmpeg -i http://remote.com/hls/segs/master.m3u8 -c:a copy -hls_time 9 -hls_list_size 3 -hls_wrap 0 -start_number 0 -hls_allow_cache 0 -segment_list_flags +live -hls_flags delete_segments ftp://ffmepg@domain.com:password@ftp.domain.com/master.m3u8`

### Split Video By Silence
`ffmpeg -i input.mkv -filter_complex "[0:a]silencedetect=n=-90dB:d=0.3[outa]" -map [outa] -f s16le -y /dev/null |& F='-aq 70 -v warning' perl -ne 'INIT { $ss=0; $se=0; } if (/silence_start: (\S+)/) { $ss=$1; $ctr+=1; printf "ffmpeg -nostdin -i input.mkv -ss %f -t %f $ENV{F} -y %03d.mkv\n", $se, ($ss-$se), $ctr; } if (/silence_end: (\S+)/) { $se=$1; } END { printf "ffmpeg -nostdin -i input.mkv -ss %f $ENV{F} -y %03d.mkv\n", $se, $ctr+1; }' | bash -x`
https://stackoverflow.com/questions/36074224/how-to-split-video-or-audio-by-silent-parts#comment63050906_36077309