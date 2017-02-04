# lane-lines-detection-canny-edge-hough-transform

<img src="white.jpg" width="480" alt="Combined Image" />

This project detects lane lines using Python and OpenCV. 
A link of the end-result video can be found at:
https://youtu.be/5z1Vx3W4QIw

## Pipeline is as follows:

* 1- Color selection: Keep only yellow and white pixels, black out all other pixels
* 2 - Convert image into grayscale
* 3 - Apply Gaussian smoothing/Gaussian blur
* 4 - Run Canny Edge Detector - I applied Otsu's method which perform clustering-based image thresholding. This method work well with the dynamic aspect of video frames
* 5- Create a rectangular region-of-interest lower-half of the image
* 6 - Run Hough Transform on the edge detected image to detect the lines
* 7 - Draw lane line by filtering Hough lines by slope and endpoint location, segragate them into right/left lane line segments. Then run linear interpolation on different right/left line segments, to create right/left lane line equations. Finaly draw right/left lane lines on the image using these equations, 

Most of the work has been to tuned the parameters for the Canny Edge Detector and Hough Transform to fit this precise problem.

## Dependencies
* Python 3
* NumPy
* OpenCV
* Matplotlib
* MoviePy

## How to run
To run the python notebook:
use Jupiter notebook
run with ``` Shift + Enter ```


For detailed explanation of what the code does, and example images of intermediate steps, refer to P1.ipynb via ```jupyter notebook```
