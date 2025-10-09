LANE MARKING AND BACKGROUND ISOLATION
## Requirements
- C++ compiler (g++)  
- OpenCV library (version 4.x preferred)

### Install OpenCV (Ubuntu/Linux)
bash
sudo apt install libopencv-dev

### how to run:
place your input image as  test_image.jpg in the same folder

### compile the program:
g++ lane_detection.cpp -o lane_detection `pkg-config --cflags --libs opencv4`

###run it:
./lane_detection

###the binary output will be saved as:
output.png

 ##  Method Used
1. Convert input image to grayscale.  
2. Apply Gaussian blur to remove noise.  
3. Detect edges using the **Canny Edge Detector**.  
4. Use **Hough Line Transform** to identify lane lines.  
5. Draw the detected lane boundaries in **black** on a white mask.  
6. Save the final binary image (`output.png`).


