# License_Plate_Detection
Real-time license plate detection using OpenCV. Suitable for GitHub.
Description for License Plate Detection Project:

This Python project utilizes computer vision techniques to detect license plates in real-time using OpenCV. The script captures video from a webcam feed and applies a Haar cascade classifier trained specifically for detecting license plates. Here's a breakdown of the project:

1. **Setup:**
   - The project begins with importing necessary libraries, including OpenCV (`cv2`) and NumPy (`numpy`).
   - Parameters such as frame width, frame height, and minimum area for plate detection are initialized.

2. **Cascade Classifier:**
   - The Haar cascade classifier for detecting Russian license plates (`haarcascade_russian_plate_number.xml`) is loaded using `cv2.CascadeClassifier`.

3. **Video Capture:**
   - The script accesses the webcam feed using `cv2.VideoCapture(0)`.
   - Parameters for frame width, frame height, and brightness are set for the video capture.

4. **Plate Detection:**
   - Inside the main loop, each frame from the webcam feed is read.
   - The frame is converted to grayscale (`imgGray`) for easier processing.
   - The `detectMultiScale` function is applied to `imgGray` to detect potential license plate areas. This function returns a list of rectangles representing the detected plates.
   - For each detected plate area, its size is compared to the minimum area threshold. If it exceeds this threshold, it is considered a valid license plate.
   - A bounding box and label ("NumberPlate") are drawn around the detected plate area on the original color image (`img`). Additionally, the region of interest (ROI) corresponding to the detected plate is extracted (`imgRoi`).

5. **Display:**
   - The resulting image with bounding boxes and labels is displayed using `cv2.imshow`.

6. **Saving Scans:**
   - If the user presses the 's' key, the script saves the detected license plate as an image in the specified directory.
   - A green rectangle with the text "Scan Saved" is overlaid on the image to indicate successful saving.

7. **Loop Control:**
   - The loop continues until the user exits by pressing any key.

8. **GitHub Repository:**
   - The code is intended to be uploaded as a GitHub repository. Proper documentation, README, and license files should be included for clarity and proper usage.

This project provides a foundation for building more sophisticated license plate recognition systems, such as vehicle tracking or access control systems, by extending it with additional functionalities like character recognition.
