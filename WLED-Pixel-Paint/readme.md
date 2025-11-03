# WLED Pixel Paint

A browser-based paint tool for 2D and 1D setups that allows you to directly draw whatever your heart desires and directly upload the result to your WLED controller.

## 2D editor

<img width="1298" height="1389" alt="image" src="https://github.com/user-attachments/assets/bcbd159c-fedd-4a90-a386-cf3a98358bb1" />

## 1D editor

<img width="833" height="1185" alt="image" src="https://github.com/user-attachments/assets/504f8241-3557-49ce-bfda-7a0bcc6f9692" />


## Features

- **Drawing Tools**
  - Brush, fill and smear (1D & 2D)
  - Line, rectangle, circle (2D only)
  - Adjustable brush size and hardness is used by all tools
  - Undo function up to 10 steps

- **Color Picker**
  - using the familiar iro.js color wheel from the main WLED UI

- **Live Preview**
  - Any change shows up on the LEDs immediately
  - Updates are sent as json commands over websocket, http as a (slow) fallback
  - Preview is highly responsive by only sending changed pixels with a full redraw when painting ends
  - By using the json interface, single segments can be painted, allowing to draw overlapping segments or multi-segment setups and backwards compatibility (tested with 0.14.4)
  - avoids parallel connections to not overwhelm the ESP, requests are sent sequentially

- **1D and 2D Modes**
  - Automatically switches between strip and matrix layout based on selected segment
  - In 1D mode, there is an overview of the full strip at the top with "zoomed" rows to set individual pixels
  - In 2D mode, the matrix size can be manually adjusted to paint higher resolution images and save them as GIFs, up to 128x128 pixels

- **Responsive Interface**
  - Works on desktop and touch devices
  - Layout automatically adjusts depending on editor mode or screen size

- **Save directly to WLED Controller**
  - Saves 1D paintings directly as WLED presets
  - 2D paintings are converted to GIF and upload directly to WLED’s filesystem

## Installation

Download the `pixelpaint.htm.gz` file, connect to your controller, go to the file editor (`ip-address/edit`) and upload the file. Open the pixel paint by navigating to `ip-address/pixelpaint.htm`.
In **WLED version 0.14** the .gz format is not supported, use the uncompressed `pixelpaint.htm` instead.
The "online" version requires an internet connection on the client side i.e. your PC or phone **NOT** the controller! It is required to download external libraries (iro.js and omggif.js).
In order to display the gif's you create you also require the WLED gif-player (2D only).

## License

Licensed under **EUPL v1.2 or later**.
Author: **@dedehai**
