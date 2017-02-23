#**Finding Lane Lines on the Road** 


##1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps:

**1.converte the images to grayscale**

**2.use Gaussian filter to Smooth images**

**3.detect edges by canny**

**4.remove edges out of laneline's region(becouse camera is installed in a fixed position on car)**

**5.get lines using Hough Transformation** 

**6.extrapolate the left and right laneline depend on the slope of lines, line in left lane has negtive slope while line in right lane has positive slope.then calculate the average of slopes and remove these which have bigger difference to the average.then fit a straight line on the points of lines,the get the vetecis of the left and right lane**


###2. Identify potential shortcomings with your current pipeline


my pipeline have constant parameters for image process, One potential shortcoming would be the pipeline will not work correctly if the car runs in different environment,such as the car run in dusk, or the car runs on the middle of two laneline.



###3. Suggest possible improvements to your pipeline

A possible improvement would be to we should have variable parameters for the pipeline which depends on the images proccessed.that is to say we should have a algorithm which can choose the right parameters.But I have no idea on how to do it.
