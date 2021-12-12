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

# Applications: 

Applications can be used in video games, and to control smart devices without using controller. They are also super useful in presentation.

In this project, we implemented a system that used camera to locate and track a fingertip of index finger. When we arbitrarily move the fingertip in the air (within range of camera view), trajectory of fingertip motion will be recorded and drawn in the video sequences and shown on the screen.

# Novelty:
We have added a feature of digit recognition using Linear SVM (Under the folder improvements)

Support vector machine constructs a hyperplane or set of hyperplanes in a high- or infinite-dimensional space, which can be used for classification, regression, or other tasks like outliers detection. Intuitively, a good separation is achieved by the hyperplane that has the largest distance to the nearest training-data point of any class (so-called functional margin), since in general the larger the margin the lower the generalization error of the classifier. Experimental results show that SVMs achieve significantly higher search accuracy than traditional query refinement schemes after just three to four rounds of relevance feedback. 

Procedure in a nutshell:

1. Load the classifier using joblib (pickle file)
2. Read the input image 
3. Convert to grayscale and apply Gaussian filtering 
4. Threshold the image
5. Find contours in the image
6. Get rectangles contains each contour 
7. 1)For each rectangular region, calculate HOG features and predict the digit using LINEAR SVM 7.1.1: DRAW 7.1.2: RESIZE 7.1.3: HOG

# Procedure:
Run the generateClassifier.py. Then run testing.py and then finally run the performRecognition.py.
