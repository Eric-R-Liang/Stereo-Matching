# Stereo Vision
In computer vision,many complex tasks revolves around construction and analysis of 3D images. This project is a rudimentary approach to create an implement a stereo vision algorithm to convert a pair of 2D images to a 3D image.
## Background and Theory
In a 2D image,pixels can be represented by their corresponding color intensity values as well as their (x,y) coordinates. Similarly,in a 3D image,the color intensity values remains constant but the pixel coordinates are represented as (x,y,z) where z is the depth of the relative pixel. Thus, the task becomes:obtaining a depth map of the 2D images, as once that information is acquired, the rest of the conversion becomes straight forward.

In a simple stereo imaging problem,such a depth map can be obtained using 2 identical cameras separated only in the __x-direction__ by a __baseline distance (b)__.

In order to obtain depth information,an important concept to grasp is __disparity__, which can be defined as the distance between 2 points in the different images that are the projections of the same point in the scene given that the two images are superimposed. A simple geometry that will help visualize the problem is in the figure below:![Proportionality Diagram](https://user-images.githubusercontent.com/46095808/78978830-74865100-7acf-11ea-935b-0fc11ce33a37.png).

A conclusive equation that can be used to calculate the depth of the image (z) is: _**z**= (b * f) / (xl - xr)_

## Dataset 
The dataset is obtained on http://vision.middlebury.edu/stereo/data/scenes2014/. A pair of 2D stereo images along with their calibration information file are obtained. The original image is shown below: 
