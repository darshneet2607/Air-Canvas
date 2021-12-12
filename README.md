# Air-Canvas
Computer Vision Project implemented with OpenCV and Numpy

We know that artists create paintings on a canvas. But what if we can paint on air just by waving our hands. So, in this project, we are going to build an air canvas using OpenCV and Python.
We’ll use color detection and segmentation techniques to achieve this objective.

OpenCV is an open-source computer vision library for performing various advanced image processing tasks.

Color detection is an image processing technique where we can detect any color in a given range of HSV color space.
Image segmentation is the process of labeling every pixel in an image, where each pixel shares the same certain characteristics.

# Project Requisites:
1. Python - 3.x 
2. OpenCV - 4.4
3. Numpy - 1.20.1

# Steps to develop Air Canvas:
1. Start reading the frames and convert the captured frames to HSV colour space.(Easy for colour detection)
2. Prepare the canvas frame and put the respective ink buttons on it. 
3. Adjust the trackbar values for finding the mask of coloured marker.
4. Preprocess the mask with morphological operations.(Erotion and dilation)
5. Detect the contours (We are detecting red node currently), find the center coordinates of largest contour and keep storing them in the array for successive frames .(Arrays for drawing points on canvas)
6. Finally draw the points stored in array on the frames and canvas

Q. What is HSV Colour Space?

HSV stands for HUE, SATURATION, and VALUE (or brightness). It is basically a cylindrical color space.

HUE – The hue encodes color information in angular dimension.

SATURATION – Saturation encodes the intensity of color.

VALUE – Value represents the brightness of the color.

# Process:
After installing the prerequisites, run the Air-canvas.py file
