# Finding Lane Lines on the Road 

This project is an introduction to apply image processing techinques such as masking, canny edge detection and hough transform to detect lanes in an image and extend them to video.

![](./test_images_output/solidYellowCurveContinuous_Detected.jpg)

In an autonomous vehicle a front mounted camera is in a fixed postion looking generating a front view of the roads and object. Lanes are of different types, width and quality. Identifying lanes with high confidence is a must for an self driving car or a truck. Hence a roboust logic is required to ensure the intended path of travel is correctly identified.

### Pipeline Development

The pipeline development consits of the following steps.

- Understand the given image or a video file.
- Gray Scale the given image.
- Applying Gaussian filter to reduce noise.
- Use Canny Edge detection to identify the edges.
- Identify the region of intrest and mask other regions
- Use Hough transform to idetify the lanes
- Perform average function to determine the co-ordinates of the lanes
- Extrapolate the co-orindates to draw the lane

The images recorded by the camera or dimensions 960 x 540. The images are imported as array of RGB colourspace. The images are converted to grayscale images. This helps in better idenfitication of lanes, since the Canny edge detection works by identifying the gradient change in the pixels

![](./test_images_output/solidWhiteCurveGrayScale.jpg)

Canny Edge detection helps in identifying the import edges defined and tuned by the threshold parameters. 
One can play around with threshold parameters. General advice is to use a ratio of 1:3 for the low to high threhold. I found the values of 50 and 150 seems to work very well for this image and video usecase.

![](./test_images_output/solidYellowCurve2Canny.jpg)

###2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


###3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
