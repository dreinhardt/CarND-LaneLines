# **Finding Lane Lines on the Road** 

## --> Please see topic 4. with my new modifications <--

---

# Reflection

## Pipelinedescription

I used the greyscale convertion as a first step
After that I used the Gausian detection
Then the Canny edge detection helped me to create lines in my picture
After that, I used a simple polygon to mask my picture
Finally, I used the Hough transformation to detect the real "lines" in my picture

For my work, I didn't used the color selection.
You can find my work within the code and computed pictures.

The modification of draw_line was very challenging and I needed help to finalize it. 
It is not finished yet, but due to of time the result is good for me.


## 2. Identify potential shortcomings with your current pipeline


The parameters must be overworked for sure!
The images and videos are very similar. A possible problem is, in case of road work and complete different kinds of lanes. These new lanes would propably crash that small algorithm and code...


## 3. Suggest possible improvements to your pipeline and Lesson

The draw_line modification was time consuming.
To play around with the filters and line drawings was the best for me and I learned a lot!


## 4. Work after first Review
- I improved my hough-detection function. It is called hough_exp_lines(..)
- To redo this, the old function hough_lines(..) can be called instead
- I added a new draw_line function. It is called draw_exp_lines(..)
-- Within draw_exp_lines the lanes are split (left/right) as you told me in your review. 
-- Furthermore, the lines are extended nearly until the middle of the picture. 
-- The lines are visible and I cut them with fixed parameters y_min and y_max within the draw_exp_lines function.

### Pictures
Unfortunately, I do not know how to place pictures in MD files.
For better presentation, I uploaded a Results.pdf and put in some pictures for you with my final results.
Furthermore, you can have a look into the folder /test_videos_output/solidYellowLeft.mp4 with my resulting video.

### Personal Notes: 
The lanes/lines are not always "in lane" and sometimes they are flickering. 
Possible a result of false/positives which I could not find out to program.
But I think, for a first project I am sufficient with the results.
I wouldn't want to sit in one of our BMW cars, using my actual Lane-Finding algorithm, but now it is a better result than before ;-)

Best regards
Dominik Reinhardt