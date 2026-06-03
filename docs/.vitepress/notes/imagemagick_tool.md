---
name: imagemagick-tool
description: >
  Create, edit, compose, and convert raster images.
---

# ImageMagick Graphic Processor

## Overview
ImageMagick is a free, open-source software suite for editing and manipulating digital images. It can read, convert, and write images in a variety of formats (over 200).

## Common CLI Commands
```bash
# Convert format (e.g., PNG to JPG)
magick input.png output.jpg

# Resize an image preserving aspect ratio
magick input.jpg -resize 800x600 output.jpg

# Rotate an image
magick input.jpg -rotate 90 output.jpg

# Apply a blur filter
magick input.jpg -blur 0x8 output.jpg
```
