---
name: ffmpeg-multimedia
description: >
  Transcode, stream, filter, and edit video and audio files.
---

# FFmpeg Multimedia Processor

## Overview
FFmpeg is the leading multimedia framework, able to decode, encode, transcode, mux, demux, stream, filter, and play pretty much anything that humans and machines have created.

## Common CLI Commands
```bash
# Transcode video to MP4 H.264
ffmpeg -i input.avi -c:v libx264 -preset fast -c:a aac output.mp4

# Extract audio from a video file
ffmpeg -i video.mp4 -vn -acodec libmp3lame -aq 2 audio.mp3

# Resize video to 720p
ffmpeg -i input.mp4 -vf scale=-1:720 -c:a copy output.mp4

# Combine audio and video
ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac -map 0:v:0 -map 1:a:0 output.mp4
```
