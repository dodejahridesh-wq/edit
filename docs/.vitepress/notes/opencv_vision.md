---
name: opencv-vision
description: >
  Real-time computer vision frame manipulations and object detection.
---

# OpenCV Computer Vision Tool

## Overview
OpenCV (Open Source Computer Vision Library) is an open-source computer vision and machine learning software library. It provides a common infrastructure for computer vision applications.

## Python Code Example
```python
import cv2

# Read an image file
img = cv2.imread('input.jpg')

# Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Save processed image
cv2.imwrite('grayscale.jpg', gray)
```
