🔴 Real-Time Red Object Detector using OpenCV :-


A simple yet powerful Python application that uses OpenCV to detect red-colored objects in real-time from a live video stream. The script identifies red objects, draws bounding boxes around them, and displays a confirmation message on the screen.

✨ Features:-


1]Real-Time Detection: Utilizes your webcam to detect objects live.

2] Color-Based Segmentation: Isolates red objects by converting the video feed to the HSV color space for more accurate color detection.

3] Bounding Boxes: Draws green rectangular boxes around all detected red objects.

4] Noise Reduction: Ignores small, insignificant contours to avoid false positives.

5] User-Friendly Display: Shows a clear "Red Object Detected" message when an object is found.

🛠️ How It Works:-



The detection process follows a classic computer vision pipeline:

1] Video Capture: The script captures video frame-by-frame from the default camera.

2] Color Space Conversion: Each frame is converted from the BGR (Blue, Green, Red) color space to HSV (Hue, Saturation, Value). The HSV space is much better for color detection because it separates color information (Hue) from lighting/intensity (Value).

3] Color Masking: A binary mask is created to isolate only the pixels that fall within a predefined range for the color red. Since red wraps around the 0/180-degree mark in the HSV space, two separate masks are created and combined.

4] Contour Detection: The script finds the continuous contours (outlines) of the white areas in the binary mask. These contours correspond to the red objects in the frame.

5] Filtering & Drawing: It filters out very small contours to reduce noise. For each significant contour found, it calculates a bounding rectangle and draws it on the original frame. A status text is then displayed.

OUTPUT :-


<img width="804" height="641" alt="Screenshot 2025-09-15 190341" src="https://github.com/user-attachments/assets/db83d36b-cc85-467d-8647-c20fba0c2213" />

📚 Technologies Used:-

1] OpenCV-Python: The core library for all computer vision tasks.

2] NumPy: Used for efficient array manipulation and handling image data.

🔧 Configuration:-  


You can easily modify the script to detect other colors or adjust the detection sensitivity:

1] Change Target Color: Modify the lower_red1, upper_red1, lower_red2, and upper_red2 NumPy arrays with the HSV values of the color you want to detect.

2] Adjust Sensitivity: Increase or decrease the value 800 in the if area > 800: line to detect larger or smaller objects, respectively.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

MADE WITH LOVE BY SANKALP SATPUTE.


---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
GOT SUPPORT BY SS TECHNOLOGIES
