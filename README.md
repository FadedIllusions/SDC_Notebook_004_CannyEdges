# SDC_Notebook_004_CannyEdges
This notebook is the second notebook corresponding to the "Computer Vision Fundamentals" of Udacity's Self-Driving Car Nanodegree, in which we begin exploring the concepts of image processing and computer vision.

The goal of edge detection is to identify the boundaries of an object in an image. 

![Canny Edges](/images/canny.png)

To do so, we must first convert to grayscale so as to have a 1D matrix. Within this grayscale image, we have a scale of values ranging from dark (0) to light (255). Sudden changes in the brightness of neighboring pixel intensities, given by the derivation ("gradient"), tend to delineate a line/edge. Computing this gradient gives us thick edges within the image, denoting note only change in pixel intensity but the rate at which they change.

With Canny Edges, we 'thin out' these gradient edges to find just the individual pixels that follow the strongest gradients. We'll, then, extend those strong edges to include pixels at a lower threshold. (Giving us our parameters to the Canny function.)
