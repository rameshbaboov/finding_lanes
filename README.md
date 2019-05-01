# Finding Lane Lines on the Road

## Finding Lane Lines on the Road

The goals / steps of this project are the following:
•	Make a pipeline that finds lane lines on the road.
•	Extract frames from Video and use pipeline to process the frames and combine the processed frames back into video.
________________________________________

## Reflection

## 1. Describe your pipeline.

* The pipeline consists of 5 steps. Each frame is executed through these steps to convert into the required output
1.	Convert to Greyscale - first step in pipeline is to convert the image into greyscale
2.	Gaussian filtering - second step is to do Gaussian filtering for smoothening of image
3.	Canny Edge Detection - third step is to do Canny edge detection
4.	Set Region of Interest - Fourth step is to set region of Interest, using vertices. Vertices are selected automatically based on the video dimensions.
5.	Apply Hough Transformation - Fifth step is to apply Hough transformation and draw line and extrapolate left and right lines separately


*  Process_Video accepts a video as parameter and process the clip and passes the clip to process_image_master. It has also a test mode to extract the first clip and see visually the ROI.  The vertices are chosen dynamically and hence this mode helps to understand if the vertices are aligned as per requirement. Test mode false process the whole video instead of first clip



## 2. Identify potential shortcomings with your current pipeline
The algorithm works better on two videos SolidWhiteRight and SolidYellowLeft, however, it often fails to detect lines for multiple clips in Challenge.mp4. Also algorithm picksup bridge edges and other lines in the road as Lane for this video


## 3. Suggest possible improvements to your pipeline
•	Working on improving the algorithm as per the comments by reviewer. “Removing lane shakiness: If we simply apply the image pipeline, the video feed has no prior knowledge of the frame before, and thus slight deviations are very obvious in the annotated output video. An easy fix is to average the current frame lines with the previous frame lines, and if one of the lanes isn’t computed properly, to substitute the prior working lane line.That way, in the next frame that a lane is detected, it can again be averaged with the older working line.
“





