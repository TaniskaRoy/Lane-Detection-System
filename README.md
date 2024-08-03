# Road-Lane-Detection
Automatic Road Lane Detection using Open Cv

1. The first step that I took was converting the image from RGB to Greyscale
2. Noise Reduction: 
The noise reduction process was performed using image smoothening via Gaussian 
Filtering on the greyscale image using a 5x5 kernel. Although the canny edge 
detection applies a 5X5 gaussian when we apply it, just wanted to be sure about not 
missing a step.
3. Edge detection, Canny edge detection was performed on the blurred image
4. Region of Interest – from the detected edges a triangle-shaped mask was created on 
the top of the canny detector to segment out the lane line region of the edges. This 
region of interest was manually segmented.
5. From the edges' cropped lines, we then perform Hough transform to identify the 
lines. The resolution of the Hough accumulator array value as 2 pixels keeping in 
mind a smaller bin gives more precision for line detection, theta value as pi/180 
radians and threshold value as 100.
6. The lines currently displayed belong to the bins which exceeded the voting 
threshold. Then using these we average out their slope and y-intercept that would 
trace out to be a single lane.
