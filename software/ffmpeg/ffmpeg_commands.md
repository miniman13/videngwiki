---
title: Useful FFMPEG Commands
description: Because we will never remember all the options
published: true
date: 2022-10-16T08:51:33.906Z
tags: foss, open source, ffmpeg, software
editor: markdown
dateCreated: 2022-10-15T18:39:11.751Z
---

# FFMPEG Commands

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

### SRT to Decklink
`ffmpeg -i srt:remote.com:port?mode=listener -f lavfi -i anullsrc=sample_rate=48000:channel_layout=mono -filter_complex "join=inputs=3:channel_layout=octagonal:map=0.0-FL|0.1-FR|1.0-FC|1.1-BL|2.0-BR|2.0-BC|2.0-SL|2.0-SR[a]" -map 0:v -map "[a]" -f decklink -pix_fmt uyvy422 -s 1920x1080 -r 60000/1001 -ar 48000 "DeckLink Duo (2)"`
https://discord.com/channels/494428283094564864/494428766525718528/939278974410952745

### Stream Static File to Youtube
> You may need to update the video parameters to meet newer Youtube recommendations for stream ingest
{.is-info}

`ffmpeg -i "input.mov" -deinterlace -vcodec libx264 
-pix_fmt yuv420p -preset medium -r 30 -g 60 -b:v 2500k 
-acodec libmp3lame -ar 44100 -threads 6 -qscale 3 -b:a 
712000 -bufsize 512k -f flv "rtmp://a.rtmp.youtube.com/live2/key"`

### Stream Local File to Facebook
> You may need to update the video parameters to meet newer Facebook recommendations for stream ingest
{.is-info}

`ffmpeg -i "input.mov" -deinterlace -vcodec libx264 
-pix_fmt yuv420p -preset medium -r 30 -g 60 -b:v 2500k 
-acodec aac -ar 44100 -threads 6 -qscale 3 -b:a 
712000 -bufsize 512k -f flv "rtmp://rtmp-api.facebook.com:80/rtmp/key"`

### Output file with all timestamps of blackframes
`ffmpeg -i "file.mp4" -t 00:00:40 -filter_complex "[0]trim=start_frame=0:end_frame=1[c];[c][0]blend=all_mode=difference,blackframe=amount=98:threshold=32" -f null - 2>&1 | grep blackframe > output.txt`
