# **Finding Lane Lines on the Road** 

## Writeup

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 
1- Check size of the video and change it if needed to 540*960
2- Convert the image to grayscale photo
3- Get the blured version of the grayscale photo by using Gaussian blur technique
4- Transfer the blured image to into Canny output to identify the edges
5- Use Hough rule to get the lines in the photo marked in Red
6- Crop the photo into the region of interest
7- Scan the cropped photo from left to right to identify points that is in red
8- get the line question of the line from the furthest two points
9- Use the line equation to extrapolate the line on the left side of the original picutre
10- Do the same(from Point 7) for the right line but scanning this time from Right to left

### 2. Identify potential shortcomings with your current pipeline

If the car is not centered in the lane, one of the lines will not be in the cropped region of interest and might lose track of the lane.

### 3. Suggest possible improvements to your pipeline

Try to use wider region of interest but with fine tuning the Hough inputs, Canny thresholds and the blur 
