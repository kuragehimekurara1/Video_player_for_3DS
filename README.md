# Video player for 3DS

## Index
* [Screenshots](https://github.com/Core-2-Extreme/Video_player_for_3DS#Screenshots)
* [Features](https://github.com/Core-2-Extreme/Video_player_for_3DS#Features)
* [Prepare videos](https://github.com/Core-2-Extreme/Video_player_for_3DS#Prepare-videos)
* [Prepare videos (advanced users)](https://github.com/Core-2-Extreme/Video_player_for_3DS#prepare-videos-advanced-users)
* [Controls](https://github.com/Core-2-Extreme/Video_player_for_3DS#Controls)
* [Supported languages](https://github.com/Core-2-Extreme/Video_player_for_3DS#Supported-languages)
* [Supported codecs](https://github.com/Core-2-Extreme/Video_player_for_3DS#Supported-codecs)
* [Links](https://github.com/Core-2-Extreme/Video_player_for_3DS#Links)
* [Build](https://github.com/Core-2-Extreme/Video_player_for_3DS#Build)
* [Recommended resolution](https://github.com/Core-2-Extreme/Video_player_for_3DS#Recommended-resolution)
* [Benchmark](https://github.com/Core-2-Extreme/Video_player_for_3DS#Benchmark)
* [Patch note](https://github.com/Core-2-Extreme/Video_player_for_3DS#Patch-note)
* [Credits](https://github.com/Core-2-Extreme/Video_player_for_3DS#Credits)
* [Donation](https://github.com/Core-2-Extreme/Video_player_for_3DS#Donation)

## Screenshots
**With multiple audio tracks support** \
<img src="https://raw.githubusercontent.com/Core-2-Extreme/Video_player_for_3DS/main/screenshots/multiple_audio_tracks.png" width="400" height="480"> \
**With subtitles** \
<img src="https://raw.githubusercontent.com/Core-2-Extreme/Video_player_for_3DS/main/screenshots/subtitles.png" width="400" height="480"> \
**With night mode** \
<img src="https://raw.githubusercontent.com/Core-2-Extreme/Video_player_for_3DS/main/screenshots/night_mode.png" width="400" height="480"> \
**And many more...**

## Features
Hardware accelerated decoding(*0)✅ \
Hardware accelerated color conversion✅ \
Multiple video codec support ✅ \
Multiple audio codec support ✅ \
Multiple Subtitle support ✅ \
Seek ✅ \
3D video(*1)✅ \
Zoom in/out video ✅ \
Move video ✅ \
File explorer ✅
Fullscreen mode ✅

⚠️ *0 New 3DS and New 2DS only \
⚠️ *1 New 3DS and 3DS only, software decoder only, in order to see 3D video as 3D \
you need to enable 3D mode in settings(settings->LCD->Screen mode->3D)

## Prepare videos
If you are advanced user, see [Recommended resolution](https://github.com/Core-2-Extreme/Video_player_for_3DS#Recommended-resolution) and [Benchmark](https://github.com/Core-2-Extreme/Video_player_for_3DS#Benchmark) for performance then use commandline in the [Prepare videos (advanced users)](https://github.com/Core-2-Extreme/Video_player_for_3DS#prepare-videos-advanced-users).

If not, you can use these tools :
* [Nintendo Video Convertor (by T0biasCZe)](https://gbatemp.net/threads/nintendo-video-convertor-video-convertor-for-3ds-and-wii.622972/)
* [VideoPlayer3DS DS Assistant (by JustScratchCoder)](https://github.com/JustScratchCoder/VideoPlayer3DS-DS-Assistant)

## Prepare videos (advanced users)
* Download [ffmpeg](https://ffmpeg.org/download.html)
  * For NEW3DS and NEW2DS type :
  * `ffmpeg -i {input_file_name} -acodec aac -vcodec libx264 -s 800x240 -preset medium -crf 25 {output_file_name}`
  * For OLD3DS and OLD2DS type :
  * `ffmpeg -i {input_file_name} -acodec aac -vcodec mpeg4 -s 400x240 -crf 25 {output_file_name}`
* Copy generated video files to your 3DS (anywhere on your SD card)

Replace `{input_file_name}` with your input file name and `{output_file_name}` with your output file name. \
e.g. : `ffmpeg -i original_video.mp4 -acodec aac -vcodec libx264 -s 800x240 -preset medium -crf 25 converted_video.mp4`

for 3D video, referer this : [How to convert your 3d video for 3DS (by T0biasCZe)](https://gbatemp.net/threads/release-video-player-for-3ds.586094/page-10#post-9575227)

## Controls
* In normal mode
  * A : Play/Pause
  * B : Stop
  * Y : Open settings menu
  * X : Select a file
  * R : Zoom in
  * L : Zoom out
  * CPAD : Move a video and/or subtitle
  * DPAD ←→ : Seek
  * DPAD ↑↓ : Change screen brightness
  * START : Back to main menu
  * SELECT : Enter fullscreen mode
  * Touch on the bar : Seek
* In fullscreen mode
  * A : Play/Pause
  * DPAD ←→ : Seek
  * DPAD ↑↓ : Change screen brightness
  * SELECT : Exit fullscreen mode

## Supported languages
* English
* Japanese/日本語
* Hungarian/Magyar (translated by vargaviktor)
* Simplified Chinese/简体中文 (translated by LITTOMA)
* Italian/Italiano (translated by dixy52-beep)
* Spanish/Español (translated by Cookiee)
* Romanian/Română (translated by Tescu48)
* Polish/Polski (translated by JustScratchCoder)

## Supported codecs
**Supported video codecs**
* AV1
* H.261
* H.262
* H.263
* H.263+
* H.264 (AVC, MPEG4 part10)
* H.265 (HEVC)
* Motion jpeg
* MPEG1video
* MPEG2video
* MPEG4 (MPEG4 part2)

**Supported audio codecs**
* aac (Advanced audio coding)
* ac3
* mp1 (MPEG audio layer 1)
* mp2 (MPEG audio layer 2)
* mp3 (MPEG audio layer 3)
* pcm audio
* ogg (Vorbis)

**Supported subtitle codecs**
* movtext
* subrip
* subviewer
(No style support)

## Links
[Discord channel](https://discord.gg/MMsAXvetpR) \
[GBAtemp thread](https://gbatemp.net/threads/release-video-player-for-3ds.586094)

## Build
If you want to build only .3dsx :
* Install [devkitpro](https://devkitpro.org/wiki/Getting_Started)
* Clone this repository
  * On windows open `build.bat`
  * On other system, type `make` (`make -j` for faster build)

If you want to build .3dsx and .cia :
* Install [devkitpro](https://devkitpro.org/wiki/Getting_Started)
* Download [bannertool](https://github.com/Steveice10/bannertool/releases) and [makerom](https://github.com/3DSGuy/Project_CTR/releases)
* Copy them in your path (e.g. in `{devkitPro_install_dir}\tools\bin`)
* Clone this repository
  * On windows open `build.bat`
  * On other system, type `make` (`make -j` for faster build)

## Recommended resolution
On NEW 3(2)DS, it is recommended to use [patched Luma3DS](https://github.com/Core-2-Extreme/Luma3DS/releases/) for better performance. 

Videos that in this resolution will be played without any problems in most of the situations.
|  Recommended resolution  | mpeg1video | mpeg2video |    H263+   |    H264    |    H265    |
| ------------------------ | ---------- | ---------- | ---------- | ---------- | ---------- |
| OLD3DS Software decoding | 400x240@30 | 400x240@30 | 400x240@24 | 256x144@24 | 256x144@10 |
| NEW3DS Software decoding | 800x240@30 | 800x240@30 | 800x240@30 | 800x240@30 | 800x240@20 |
| NEW3DS Hardware decoding |    none    |    none    |    none    | 800x240@60 |    none    |


Videos that in this resolution may be played without problems if video is not moving a lot.
|    Maximum resolution    | mpeg1video | mpeg2video |    H263+   |    H264    |    H265    |
| ------------------------ | ---------- | ---------- | ---------- | ---------- | ---------- |
| OLD3DS Software decoding | 800x240@24 | 800x240@24 | 800x240@20 | 400x240@15 | 256x144@20 |
| NEW3DS Software decoding | 800x480@30 | 800x480@30 | 800x480@30 | 800x480@24 | 800x240@30 |
| NEW3DS Hardware decoding |    none    |    none    |    none    |1280x720@20 |    none    |

**Note : Video resolution that exceeds screen resolution (400x240 on OLD2DS, 800x240 on OLD3DS, NEW2DS and NEW3DS) has little visible effect.**

## Benchmark
⚠️ Decoding speed depends on encoder option, video type, video scene, etc... \
⚠️ This table shows average fps, so you may hear stutter audio if you use this framerate. \
(Lower video resolution or framerate in that case) \
Software decoding in this table uses only one thread not multi-threaded decoding.

**MPEG1video** \
MPEG1video test file was encoded following command : \
ffmpeg -i {input_file_name} -acodec copy -vcodec mpeg1video -s {width}x{height} -r 30 -q:v 15 {output_file_name}

|        MPEG1video        | 256x144 (144p) | 426x240 (240p) | 640x360 (360p) | 800x240 | 854x480 (480p) |
| ------------------------ | -------------- | -------------- | -------------- | ------- | -------------- |
| OLD3DS Software decoding |     69.0fps    |     39.9fps    |     24.0fps    | 27.4fps |     16.7fps    |
| NEW3DS Software decoding |    532.0fps    |    267.2fps    |    119.8fps    |158.0fps |     69.4fps    |

**MPEG2video** \
MPEG2video test file was encoded following command : \
ffmpeg -i {input_file_name} -acodec copy -vcodec mpeg2video -s {width}x{height} -r 30 -q:v 15 {output_file_name}

|        MPEG2video        | 256x144 (144p) | 426x240 (240p) | 640x360 (360p) | 800x240 | 854x480 (480p) |
| ------------------------ | -------------- | -------------- | -------------- | ------- | -------------- |
| OLD3DS Software decoding |     67.1fps    |     37.6fps    |     22.3fps    | 26.3fps |     15.4fps    |
| NEW3DS Software decoding |    518.8fps    |    254.2fps    |    113.9fps    |145.7fps |     65.9fps    |

**H263+** \
H263+ test file was encoded following command : \
ffmpeg -i {input_file_name} -acodec copy -vcodec h263p -s {width}x{height} -r 30 -q:v 15 {output_file_name}

|          H.263+          | 256x144 (144p) | 424x240 (240p) | 640x360 (360p) | 800x240 | 856x480 (480p) |
| ------------------------ | -------------- | -------------- | -------------- | ------- | -------------- |
| OLD3DS Software decoding |     62.8fps    |     35.6fps    |     21.1fps    | 24.6fps |      8.7fps    |
| NEW3DS Software decoding |    527.9fps    |    257.8fps    |    113.1fps    |144.2fps |     33.9fps    |

**H264** \
H264 test file was encoded following command : \
ffmpeg -i {input_file_name} -acodec copy -vcodec libx264 -s {width}x{height} -r 30 -preset fast -profile:v baseline  {output_file_name}

|          H.264           | 256x144 (144p) | 426x240 (240p) | 640x360 (360p) | 800x240 | 854x480 (480p) |
| ------------------------ | -------------- | -------------- | -------------- | ------- | -------------- |
| OLD3DS Software decoding |     30.7fps    |     15.9fps    |      8.8fps    | 10.2fps |      5.4fps    |
| NEW3DS Software decoding |    226.7fps    |     95.1fps    |     43.4fps    | 53.2fps |     25.1fps    |
| NEW3DS Hardware decoding |    560.6fps    |    338.7fps    |    206.0fps    |235.3fps |    114.7fps    |

**H265** \
H265 test file was encoded following command : \
ffmpeg -i {input_file_name} -acodec copy -vcodec libx265 -s {width}x{height} -r 30 -preset fast -profile:v main  {output_file_name}

|          H.265           | 256x144 (144p) | 426x240 (240p) | 640x360 (360p) | 800x240 | 854x480 (480p) |
| ------------------------ | -------------- | -------------- | -------------- | ------- | -------------- |
| OLD3DS Software decoding |     22.4fps    |     11.3fps    |      6.2fps    |  7.2fps |      3.9fps    |
| NEW3DS Software decoding |    136.8fps    |     55.7fps    |     26.4fps    | 30.9fps |     15.3fps    |

## Patch note
* [v1.5.2](https://github.com/Core-2-Extreme/Video_player_for_3DS#v152)
* [v1.5.1](https://github.com/Core-2-Extreme/Video_player_for_3DS#v151)
* [v1.5.0](https://github.com/Core-2-Extreme/Video_player_for_3DS#v150)
* [v1.4.2](https://github.com/Core-2-Extreme/Video_player_for_3DS#v142)
* [v1.4.1](https://github.com/Core-2-Extreme/Video_player_for_3DS#v141)
* [v1.4.0](https://github.com/Core-2-Extreme/Video_player_for_3DS#v140)
* [v1.3.3](https://github.com/Core-2-Extreme/Video_player_for_3DS#v133)
* [v1.3.2](https://github.com/Core-2-Extreme/Video_player_for_3DS#v132)
* [v1.3.1](https://github.com/Core-2-Extreme/Video_player_for_3DS#v131)
* [v1.3.0](https://github.com/Core-2-Extreme/Video_player_for_3DS#v130)
* [v1.2.0](https://github.com/Core-2-Extreme/Video_player_for_3DS#v120)
* [v1.1.1](https://github.com/Core-2-Extreme/Video_player_for_3DS#v111)
* [v1.1.0](https://github.com/Core-2-Extreme/Video_player_for_3DS#v110)
* [v1.0.1](https://github.com/Core-2-Extreme/Video_player_for_3DS#v101)
* [v1.0.0](https://github.com/Core-2-Extreme/Video_player_for_3DS#v100)

### v1.5.2
**Changes** \
Ignore unsupported codec so that you can play supported codec only \
(e.g. You can now play videos that contain unsupported subtitles/audio)

**Fixed bugs** \
Hardware decoder won't play videos that contain B-frames smoothly has been fixed \
(It means you don't have to care about B-frames when encoding to H.264 videos)

### v1.5.1
**Added features** \
Screen update frequency in audio only files have been increased \
Performance has been improved by adding DMA \
Video playback is automatically paused when runs out of buffer \
(You can change threshold by changing 'Restart playback threshold' settings) \
Seeking speed has been improved

**Changes** \
Disallow sleep when only headset is connected \
(allow sleep if headset is disconnected during playback) \
App directory has been changed from sdmc:/Video_player/ to sdmc:/3ds/Video_player/ \
(App will automatically move folder) \
Simplified Chinese(简体中文) translation has been updated \
Enabled 'correct aspect ratio option' by default

**Fixed bugs** \
Crashes in hw decoder in some videos have been fixed \
Automatically enter full screen mode even file explorer is opened has been fixed \
App will freeze if you seek after EOF has been fixed \
Unable to pause/resume in tagged mp3 has been fixed \
Video position won't be saved in some cases have been fixed \
Glitch on video in full screen mode has been fixed \
Some directories can't be entered have been fixed \
Some videos won't be played at correct speed has been fixed \
Frame desync in some 3D videos have been fixed


### v1.5.0
Subtitles have been supported (*0) \
Disable video, audio and subtitle have been added \
Audio desync has been fixed \
AV1 videos have been supported \
The problem some video won't play smoothly in sw decoder has been fixed \
Screen brightness adjustment function has been added (DPAD "↑" and "↓") \
*0 No style support, only plain text \
Other minor changes

### v1.4.2
Unexpected touch in Nintendo's home menu has been fixed \
Multi-threaded decoding stability has been fixed and it is enabled by default \
Seeking stability has been fixed \
Repeat, in order, random playback mode have been added \
Other minor changes

### v1.4.1
The "FSUSER_OpenFile() failed" error has been fixed \
Adjusted font and button size in settings menu \
Multi-threaded decoding is disabled by default because it has stability problem \
Polish(Polski) translation has been added (by JustScratchCoder) \
Other minor changes

### v1.4.0
Decoded image(raw) buffer has been added and it makes playback \
much much much much better (especially on OLD3DS)
Spanish(español) translation has been added (by Cookiee) \
Romanian(Română) translation has been added (by Tescu48) \
Other minor changes

### v1.3.3
'aspect ratio 10:3 mode' has been changed to 'correct aspect ratio mode' (follow sar value(*0)) \
Color conversion speed has been improved \
Simplified Chinese(简体中文) translation has been added (by LITTOMA) \
Italian(italiano) translation has been added (by dixy52-beep) \
*0 if video size is 800x240 and no sar value is set, it autmatically apply sar 1:2 \
Other minor changes

### v1.3.2
Added aspect ratio 10:3 mode (for 800x240 videos) \
Added disable resize and move video mode \
Added remember video pos mode (resume from that pos next time) \
Other minor changes

### v1.3.1
Volume adjustment has been added (from 0% to 999%) \
Direction pad seeking has been added (from 1 second to 99 seconds) \
Hungarian(magyar) translation has been added (by vargaviktor) \
Other minor changes

### v1.3.0
The video that has more than one audio tracks has been supported (Press Y key-> select audio track to select track) \
Multi-threaded decoding has been supported (Press Y key-> use multi-threaded decoding to toggle) \
Hardware decoder has been merged (Press Y key-> use hw decoder to toggle) \
Full screen mode has been supported (Press select key to toggle) \
Other minor changes

### v1.2.0
Hardware decoding won't work in .cia has been fixed \
Hardware decoding won't work in some resolution has been fixed \
Added hardware color conversion for software decoder \
Added 3D video support(software decoder only) \
Other minor changes and optimization

### v1.1.1
Video will not be decoded correctly in hardware decoder has been fixed

### v1.1.0
Added hardware decoder (β)

### v1.0.1
Added allow skip frames option

### v1.0.0
Initial release

## Credits
* Core 2 Extreme
* dixy52-beep (icon, banner, in app texture, Italian translation)
* windows-server-2003 (bug fix)
* vargaviktor (Hungarian translation)
* HIDE810 (bug fix)
* LITTOMA (Simplified chinese translation)
* Cookiee (Spanish translation)
* Tescu48 (Romanian translation)
* JustScratchCoder (Polish translation)

## Donation
If you find my app helpful, buy me a cup of coffee.
* BTC : bc1qch33qdce5hwxte0pm8pn0a6qqnartg2ujklhhc
* LTC : MKTD3U2vCMi7S7Jb1EQ2FiS4AdHC23PxJh
