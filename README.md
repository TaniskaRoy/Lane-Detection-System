# Lane-Detection-System


## Project Overview

This project involves developing an **automatic road lane detection system** using **OpenCV**. The system processes road images to identify and highlight the lane lines, which is a crucial feature for **autonomous vehicles** and **lane-keeping assist systems**.

### Key Steps in the Process:
1. **RGB to Greyscale Conversion**: The image is first converted from RGB to greyscale to simplify the image data for further processing.
2. **Noise Reduction**: Gaussian filtering with a 5x5 kernel is applied for noise reduction to smoothen the greyscale image.
3. **Edge Detection**: **Canny edge detection** is applied to detect the edges in the image.
4. **Region of Interest (ROI)**: A triangle-shaped mask is manually created to focus on the region of the image containing the lane lines. This region is then segmented out from the detected edges.
5. **Hough Transform**: The **Hough Transform** is used to detect straight lines in the image. The Hough accumulator array has a resolution of 2 pixels, theta value as **π/180 radians**, and a threshold of 100 to ensure precision in line detection.
6. **Lane Mapping**: Detected lines are averaged based on their slopes and y-intercepts to trace out a single lane line.

### Key Features:
- **Automatic Road Lane Detection** using OpenCV.
- **Image Preprocessing**: RGB to greyscale conversion, noise reduction via Gaussian filtering.
- **Edge Detection** using Canny edge detection.
- **Lane Line Identification** using Hough Transform with fine-tuned parameters.
- **Lane Mapping**: Averaging slopes and intercepts to draw accurate lane lines.

## Files in the Project

1. **Road Lane Detection.ipynb**: The Jupyter Notebook containing the code for lane detection using OpenCV.
2. **Road_Pic.jpg**: The sample road image that is passed through the lane detection model to detect lane lines.

## Applications

The road lane detection system can be applied in various fields, including:
- **Autonomous Vehicles**: For lane-keeping assist systems to ensure the vehicle stays within its lane.
- **Driver Assistance Systems**: To alert drivers when they unintentionally drift out of their lane.
- **Smart Transportation Systems**: For real-time traffic analysis and route navigation.
- **Advanced Driver Assistance Systems (ADAS)**: Enhancing safety by providing lane recognition as part of a broader system to assist drivers.

## Conclusion

The automatic road lane detection system improves lane-keeping assist systems, contributing to better safety and accuracy in autonomous vehicles and driver assistance technology. By using techniques like Canny edge detection and Hough Transform, the system efficiently detects and maps lane lines, which can be further applied to real-world transportation technologies.
