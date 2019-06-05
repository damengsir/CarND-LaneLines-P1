# **Finding Lane Lines on the Road** 

## Writeup Template


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline.

My pipeline consisted of 6 steps：
1. Convert the images to grayscale.
2. Define a kernel size for Gaussian smoothing.
3. Extract the edge using Canny function.
4. Coding up a Region of Interest Mask.
5. Draw lane lines using segmented lines.
6. Draw lane lines using solid lines.


In order to include only lane edges, I'v modified the position of several points in region_of_interest() function.

In order to reduce the shake of pipelines in videos, I'v reduced the value of "minLineLength" and "macLineGap" in HoughLinesP() function.


### 2. Identify potential shortcomings with your current pipeline


The two pipelines will get crossed easyly when the road ahead appears a big curve. 


### 3. Suggest possible improvements to your pipeline
When there is a curve in the road ahead,we can draw curve by changing the model.

