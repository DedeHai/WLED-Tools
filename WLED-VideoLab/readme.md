# WLED VideoLab

A browser-based video streaming tool with integrated loop-control and GIF export

## Features

- **Video Streaming**
  - Uses DDP protocol over websocket for fast streaming to thousands of pixels at high frame rates
  - Stream vidoes to your 2D LED matrix or 1D Strip
  - Supports selecting videos on the client device or streaming directly from a CORS enabled URL like pixabay (youtube and similar do not support this unfortunately)
  - Adjust playback speed as well as start/stop time of the loop
  - Works in AP mode!

- **Filtering**
  - Select the area of the video you want to stream to the LEDs
  - Live adjust brightness, gamma-correction and dark-pixel-cutoff
  - Optionally choose a background color

- **Save your work**
  - Store current settings as "video presets" to quickly load URLs and all settings. Limitation: currently stored in browser cache only.
  - Export a video loop as an animated GIF: choose FPS and color resolution to generate smaller files
  - Download the generated GIF to your device or upload it to the controller with a single click

- **Limitations and known issues**
  - Only works on a recent WLED 0.16 build (requires DDP over WS)
  - Camera access & streaming is not possible unfortunately due to browser security restrictions
  - Control on mobile devices is a bit finiky and needs improvement
  - Loop control and progress-bar can stop responding properly, reload the page if that happens
  - GIF export on long loops can hang, reload and reduce time interval or FPS
  - Currently generating GIFs does not work in AP mode but it will in the future
  - Not tested on all browsers

## Installation

Download the `videolab.htm.gz` file, connect to your controller, go to the file editor (`ip-address/edit`) and upload the file. Open it by navigating to `ip-address/videolab.htm`.

## License

Licensed under **EUPL v1.2 or later**.
Author: **@dedehai**

## Changelog

### Version 0.9B
beta release
