**Finding Lane Lines on the Road**

The goals / steps of this project are the following:

* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report
Reflection

My pipeline consisted as the following: 

1) First, I converted the images to grayscale, 


2)  I selected Gaussian Blur function with kernel size = 5, then i applied canny function with low threshold = 50 and high threshold = 150.

3) I defined four sided polygon for selected region (450, 320),(490, 320), then apply vertices on the out of canny image which is called edges in the program




4) apply HoughLines with these best practies parameters ( rho = 2, theta = np.pi/180, threshold = 60, min_line_length = 100, max_line_gap = 150), the draw lines on a blank image 







5) combine the lines blank image with initial image which is without any processing 



In order to draw a single line on the left and right lanes, I modified the draw_lines() function by  choose red color=[255, 0, 0], the thickness=8 .


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when in a highly carved road the two line intersect with each so I decreased the rectangle.

Another shortcoming could be in highly intersection between lines in challenge video it could be solved by changing rectangle topology?

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to make the draw line more visible ...

Another potential improvement could be to draw rectangle between two lines ...

